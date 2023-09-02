# min_stacK

class MinStack {
public:
    stack<int>st,s2; //st=stack  s2=minstack(for storing min value)
    MinStack() {
        
    }
    
    void push(int val) {
        st.push(val);
        if(s2.empty()|| val<=s2.top())
            s2.push(val);
    }
    
    void pop() {
        
        if(st.top()==s2.top())
            s2.pop();
        st.pop();
        
    }
    
    int top() {
        return st.top();
    }
    
    int getMin() {
        return  s2.top(); //min stack's top
    }
};

/**
 * Your MinStack object will be instantiated and called as such:
 * MinStack* obj = new MinStack();
 * obj->push(val);
 * obj->pop();
 * int param_3 = obj->top();
 * int param_4 = obj->getMin();
 */
