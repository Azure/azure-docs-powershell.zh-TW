---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 67cffe7f0cdaebc655eb98321166bb7805844a5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454400"
---
# <span data-ttu-id="e2e12-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="e2e12-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="e2e12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2e12-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e12-103">更新特定 AAD 實體的資料 Lake Analytics 計算原則規則。</span><span class="sxs-lookup"><span data-stu-id="e2e12-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2e12-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2e12-104">SYNTAX</span></span>

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2e12-105">說明</span><span class="sxs-lookup"><span data-stu-id="e2e12-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e12-106">**更新-AzureRmDataLakeAnalyticsComputePolicy** 會針對 Azure Data Lake Analytics 帳戶中的特定 AAD 實體更新指定的計算原則規則。</span><span class="sxs-lookup"><span data-stu-id="e2e12-106">The **Update-AzureRmDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e2e12-107">示例</span><span class="sxs-lookup"><span data-stu-id="e2e12-107">EXAMPLES</span></span>

### <span data-ttu-id="e2e12-108">範例1：在計算原則中更新一個規則</span><span class="sxs-lookup"><span data-stu-id="e2e12-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="e2e12-109">這個命令會更新帳戶「contosoadla」中名為「myPolicy」的原則，以確保使用者無法提交超過5個以上並行度的任何作業。</span><span class="sxs-lookup"><span data-stu-id="e2e12-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="e2e12-110">範例2：建立兩個規則更新的計算原則</span><span class="sxs-lookup"><span data-stu-id="e2e12-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="e2e12-111">這個命令會在帳戶 "contosoadla" 中建立名為 "myPolicy" 的原則，以確保使用者無法提交超過5個並行度或優先順序低於100的任何作業。</span><span class="sxs-lookup"><span data-stu-id="e2e12-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="e2e12-112">參數</span><span class="sxs-lookup"><span data-stu-id="e2e12-112">PARAMETERS</span></span>

### <span data-ttu-id="e2e12-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e2e12-113">-Account</span></span>
<span data-ttu-id="e2e12-114">要在其中更新計算原則的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e2e12-114">Name of the account to update the compute policy in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e12-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="e2e12-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="e2e12-116">此原則的每個作業支援的最大並行度。</span><span class="sxs-lookup"><span data-stu-id="e2e12-116">The maximum supported degree of parallelism per job for this policy.</span></span> <span data-ttu-id="e2e12-117">必須指定 this、MinPriorityPerJob 或這兩個參數。</span><span class="sxs-lookup"><span data-stu-id="e2e12-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e12-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="e2e12-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="e2e12-119">此原則的每個作業支援的最低優先順序。</span><span class="sxs-lookup"><span data-stu-id="e2e12-119">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="e2e12-120">必須指定 this、MaxDegreeOfParallelismPerJob 或這兩個參數。</span><span class="sxs-lookup"><span data-stu-id="e2e12-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e12-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2e12-121">-Name</span></span>
<span data-ttu-id="e2e12-122">要更新之計算原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2e12-122">Name of the compute policy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e12-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2e12-123">-ResourceGroupName</span></span>
<span data-ttu-id="e2e12-124">您帳戶所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2e12-124">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="e2e12-125">[選用]，如果未提供，就會嘗試探索。</span><span class="sxs-lookup"><span data-stu-id="e2e12-125">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e12-126">-確認</span><span class="sxs-lookup"><span data-stu-id="e2e12-126">-Confirm</span></span>
<span data-ttu-id="e2e12-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e2e12-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e12-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2e12-128">-WhatIf</span></span>
<span data-ttu-id="e2e12-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e2e12-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2e12-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2e12-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e12-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e12-131">-DefaultProfile</span></span>
<span data-ttu-id="e2e12-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2e12-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e12-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e12-133">CommonParameters</span></span>
<span data-ttu-id="e2e12-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2e12-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e12-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e2e12-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e12-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e2e12-136">INPUTS</span></span>

### <span data-ttu-id="e2e12-137">System.object</span><span class="sxs-lookup"><span data-stu-id="e2e12-137">System.String</span></span>
<span data-ttu-id="e2e12-138">System.object</span><span class="sxs-lookup"><span data-stu-id="e2e12-138">System.Int32</span></span>

## <span data-ttu-id="e2e12-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e2e12-139">OUTPUTS</span></span>

### <span data-ttu-id="e2e12-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="e2e12-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="e2e12-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e2e12-141">NOTES</span></span>

## <span data-ttu-id="e2e12-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2e12-142">RELATED LINKS</span></span>

