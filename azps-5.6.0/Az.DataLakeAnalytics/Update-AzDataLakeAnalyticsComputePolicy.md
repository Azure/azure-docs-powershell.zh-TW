---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: c27319e368223b00ba17caf9d408e6a1010c766d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912897"
---
# <span data-ttu-id="3c94b-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="3c94b-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="3c94b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3c94b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c94b-103">更新特定 AAD 實體的 Data Lake Analytics 計算原則規則。</span><span class="sxs-lookup"><span data-stu-id="3c94b-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="3c94b-104">語法</span><span class="sxs-lookup"><span data-stu-id="3c94b-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c94b-105">描述</span><span class="sxs-lookup"><span data-stu-id="3c94b-105">DESCRIPTION</span></span>
<span data-ttu-id="3c94b-106">**Update-AzDataLakeAnalyticsComputePolicy** 會更新 Azure Data Lake Analytics 帳戶中特定 AAD 實體的指定計算原則規則。</span><span class="sxs-lookup"><span data-stu-id="3c94b-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="3c94b-107">例子</span><span class="sxs-lookup"><span data-stu-id="3c94b-107">EXAMPLES</span></span>

### <span data-ttu-id="3c94b-108">範例 1：更新計算原則中的一個規則</span><span class="sxs-lookup"><span data-stu-id="3c94b-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="3c94b-109">此命令會更新帳戶 "contodla" 中稱為「myPolicy」的一項政策，以確保使用者無法提交超過 5 個分析單位的工作。</span><span class="sxs-lookup"><span data-stu-id="3c94b-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="3c94b-110">範例 2：使用兩個規則更新建立計算原則</span><span class="sxs-lookup"><span data-stu-id="3c94b-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="3c94b-111">此命令在帳戶 "contola" 中建立一個稱為「myPolicy」的策略，以確保使用者無法提交超過 5 個分析單位或優先順序低於 100 的工作</span><span class="sxs-lookup"><span data-stu-id="3c94b-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="3c94b-112">參數</span><span class="sxs-lookup"><span data-stu-id="3c94b-112">PARAMETERS</span></span>

### <span data-ttu-id="3c94b-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="3c94b-113">-Account</span></span>
<span data-ttu-id="3c94b-114">要更新計算策略的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3c94b-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="3c94b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c94b-115">-DefaultProfile</span></span>
<span data-ttu-id="3c94b-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="3c94b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c94b-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="3c94b-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="3c94b-118">此政策每個工作支援的最大分析單位。</span><span class="sxs-lookup"><span data-stu-id="3c94b-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="3c94b-119">您必須指定此、MinPriorityPerJob 或兩個參數。</span><span class="sxs-lookup"><span data-stu-id="3c94b-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c94b-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="3c94b-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="3c94b-121">此政策每個工作的最低支援優先順序。</span><span class="sxs-lookup"><span data-stu-id="3c94b-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="3c94b-122">無論是此選項、MaxAnalyticsUnitsPerJob，或必須指定這兩個參數。</span><span class="sxs-lookup"><span data-stu-id="3c94b-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="3c94b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c94b-123">-Name</span></span>
<span data-ttu-id="3c94b-124">要更新的計算策略名稱。</span><span class="sxs-lookup"><span data-stu-id="3c94b-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="3c94b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c94b-125">-ResourceGroupName</span></span>
<span data-ttu-id="3c94b-126">您帳戶存在下的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3c94b-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="3c94b-127">選擇性，並嘗試探索是否未提供。</span><span class="sxs-lookup"><span data-stu-id="3c94b-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="3c94b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="3c94b-128">-Confirm</span></span>
<span data-ttu-id="3c94b-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3c94b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c94b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c94b-130">-WhatIf</span></span>
<span data-ttu-id="3c94b-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3c94b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c94b-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c94b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c94b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c94b-133">CommonParameters</span></span>
<span data-ttu-id="3c94b-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3c94b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c94b-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3c94b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c94b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="3c94b-136">INPUTS</span></span>

### <span data-ttu-id="3c94b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3c94b-137">System.String</span></span>

### <span data-ttu-id="3c94b-138">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3c94b-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3c94b-139">輸出</span><span class="sxs-lookup"><span data-stu-id="3c94b-139">OUTPUTS</span></span>

### <span data-ttu-id="3c94b-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="3c94b-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="3c94b-141">筆記</span><span class="sxs-lookup"><span data-stu-id="3c94b-141">NOTES</span></span>

## <span data-ttu-id="3c94b-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c94b-142">RELATED LINKS</span></span>
