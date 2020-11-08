---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969305"
---
# <span data-ttu-id="18a91-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="18a91-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="18a91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18a91-102">SYNOPSIS</span></span>
<span data-ttu-id="18a91-103">更新特定 AAD 實體的資料 Lake Analytics 計算原則規則。</span><span class="sxs-lookup"><span data-stu-id="18a91-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="18a91-104">句法</span><span class="sxs-lookup"><span data-stu-id="18a91-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18a91-105">說明</span><span class="sxs-lookup"><span data-stu-id="18a91-105">DESCRIPTION</span></span>
<span data-ttu-id="18a91-106">**更新-AzDataLakeAnalyticsComputePolicy** 會針對 Azure Data Lake Analytics 帳戶中的特定 AAD 實體更新指定的計算原則規則。</span><span class="sxs-lookup"><span data-stu-id="18a91-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="18a91-107">示例</span><span class="sxs-lookup"><span data-stu-id="18a91-107">EXAMPLES</span></span>

### <span data-ttu-id="18a91-108">範例1：在計算原則中更新一個規則</span><span class="sxs-lookup"><span data-stu-id="18a91-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="18a91-109">這個命令會更新帳戶「contosoadla」中名為「myPolicy」的原則，以確保使用者無法提交超過5個分析單元的任何作業。</span><span class="sxs-lookup"><span data-stu-id="18a91-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="18a91-110">範例2：建立兩個規則更新的計算原則</span><span class="sxs-lookup"><span data-stu-id="18a91-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="18a91-111">這個命令會在帳戶 "contosoadla" 中建立名為 "myPolicy" 的原則，以確保使用者無法提交超過5個分析單元或優先順序低於100的任何作業</span><span class="sxs-lookup"><span data-stu-id="18a91-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="18a91-112">參數</span><span class="sxs-lookup"><span data-stu-id="18a91-112">PARAMETERS</span></span>

### <span data-ttu-id="18a91-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="18a91-113">-Account</span></span>
<span data-ttu-id="18a91-114">要在其中更新計算原則的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="18a91-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="18a91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a91-115">-DefaultProfile</span></span>
<span data-ttu-id="18a91-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="18a91-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18a91-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="18a91-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="18a91-118">此原則每個作業支援的分析單位上限。</span><span class="sxs-lookup"><span data-stu-id="18a91-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="18a91-119">必須指定 this、MinPriorityPerJob 或這兩個參數。</span><span class="sxs-lookup"><span data-stu-id="18a91-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="18a91-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="18a91-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="18a91-121">此原則的每個作業支援的最低優先順序。</span><span class="sxs-lookup"><span data-stu-id="18a91-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="18a91-122">必須指定 this、MaxAnalyticsUnitsPerJob 或這兩個參數。</span><span class="sxs-lookup"><span data-stu-id="18a91-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="18a91-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="18a91-123">-Name</span></span>
<span data-ttu-id="18a91-124">要更新之計算原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="18a91-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="18a91-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18a91-125">-ResourceGroupName</span></span>
<span data-ttu-id="18a91-126">您帳戶所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="18a91-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="18a91-127">[選用]，如果未提供，就會嘗試探索。</span><span class="sxs-lookup"><span data-stu-id="18a91-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="18a91-128">-確認</span><span class="sxs-lookup"><span data-stu-id="18a91-128">-Confirm</span></span>
<span data-ttu-id="18a91-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="18a91-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18a91-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18a91-130">-WhatIf</span></span>
<span data-ttu-id="18a91-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="18a91-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18a91-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="18a91-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18a91-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a91-133">CommonParameters</span></span>
<span data-ttu-id="18a91-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18a91-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a91-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="18a91-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a91-136">輸入</span><span class="sxs-lookup"><span data-stu-id="18a91-136">INPUTS</span></span>

### <span data-ttu-id="18a91-137">System.object</span><span class="sxs-lookup"><span data-stu-id="18a91-137">System.String</span></span>

### <span data-ttu-id="18a91-138">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="18a91-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="18a91-139">輸出</span><span class="sxs-lookup"><span data-stu-id="18a91-139">OUTPUTS</span></span>

### <span data-ttu-id="18a91-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="18a91-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="18a91-141">筆記</span><span class="sxs-lookup"><span data-stu-id="18a91-141">NOTES</span></span>

## <span data-ttu-id="18a91-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="18a91-142">RELATED LINKS</span></span>
