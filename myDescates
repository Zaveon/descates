class DescartesUtils {

    /**
     * 如果传入的参数只有一个数组，求笛卡尔积结果
     * @param arr1 一维数组
     * @returns {Array}
     */
    static descartes1(arr1){
        // 返回结果，是一个二维数组
        let result = [];
        let i = 0;
        for (i = 0; i < arr1.length; i++) {
            let item1 = arr1[i];
            result.push([item1]);
        }
        return result;
    }

    /**
     * 如果传入的参数只有两个数组，求笛卡尔积结果
     * @param arr1 一维数组
     * @param arr2 一维数组
     * @returns {Array}
     */
    static descartes2(arr1, arr2) {
        // 返回结果，是一个二维数组
        let result = [];
        let i = 0, j = 0;
        for (i = 0; i < arr1.length; i++) {
            let item1 = arr1[i];
            for (j = 0; j < arr2.length; j++) {
                let item2 = arr2[j];
                result.push([item1, item2]);
            }
        }
        return result;
    }

    /**
     *
     * @param arr2D 二维数组
     * @param arr1D 一维数组
     * @returns {Array}
     */
    static descartes2DAnd1D(arr2D, arr1D) {
        let i = 0, j = 0;
        // 返回结果，是一个二维数组
        let result = [];

        for (i = 0; i < arr2D.length; i++) {
            let arrOf2D = arr2D[i];
            for (j = 0; j < arr1D.length; j++) {
                let item1D = arr1D[j];
                result.push(arrOf2D.concat(item1D));
            }
        }

        return result;
    }

    static descartes3(list) {
        let listLength = list.length;
        let i = 0, j = 0;
        // 返回结果，是一个二维数组
        let result = [];
        // 为了便于观察，采用这种顺序
        let arr2D = DescartesUtils.descartes2(list[0], list[1]);
        for (i = 2; i < listLength; i++) {
            let arrOfList = list[i];
            arr2D = DescartesUtils.descartes2DAnd1D(arr2D, arrOfList);
        }
        return arr2D;
    }

    //笛卡儿积组合
    static descartes(list)
    {
        if (!list) {
            return [];
        }
        if (list.length <= 0) {
            return [];
        }
        if (list.length === 1) {
            return DescartesUtils.descartes1(list[0]);
        }
        if (list.length === 2) {
            return DescartesUtils.descartes2(list[0], list[1]);
        }
        if (list.length >= 3) {
            return DescartesUtils.descartes3(list);
        }
    }

}

export default DescartesUtils
