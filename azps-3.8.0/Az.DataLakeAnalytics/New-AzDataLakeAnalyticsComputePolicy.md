---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 76df1cb780220a09ccc0d571fd88223e746eefe6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956782"
---
# <span data-ttu-id="23d98-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="23d98-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="23d98-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23d98-102">SYNOPSIS</span></span>
<span data-ttu-id="23d98-103">建立特定 AAD 實體的資料 Lake Analytics 計算原則規則。</span><span class="sxs-lookup"><span data-stu-id="23d98-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="23d98-104">句法</span><span class="sxs-lookup"><span data-stu-id="23d98-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23d98-105">說明</span><span class="sxs-lookup"><span data-stu-id="23d98-105">DESCRIPTION</span></span>
<span data-ttu-id="23d98-106">**新-AzDataLakeAnalyticsComputePolicy** 會針對 Azure Data Lake Analytics 帳戶中的特定 AAD 實體建立指定的計算原則規則。</span><span class="sxs-lookup"><span data-stu-id="23d98-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="23d98-107">示例</span><span class="sxs-lookup"><span data-stu-id="23d98-107">EXAMPLES</span></span>

### <span data-ttu-id="23d98-108">範例1：建立只有一個規則的計算原則</span><span class="sxs-lookup"><span data-stu-id="23d98-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="23d98-109">這個命令會在帳戶 "contosoadla" 中針對 id 為 "83cb7ad2-3523-4b82-b909-d478b0d8aea3" 的使用者建立名為 "myPolicy" 的原則，以確保他們無法提交超過5個分析單元的任何作業。</span><span class="sxs-lookup"><span data-stu-id="23d98-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="23d98-110">範例2：建立兩個規則集的計算原則</span><span class="sxs-lookup"><span data-stu-id="23d98-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="23d98-111">這個命令會針對 id 為「83cb7ad2-3523-4b82-b909-d478b0d8aea3」的使用者建立名為 "contosoadla" 的原則 "myPolicy"，以確保他們無法提交超過5個分析單元或優先順序低於100的任何作業。</span><span class="sxs-lookup"><span data-stu-id="23d98-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="23d98-112">參數</span><span class="sxs-lookup"><span data-stu-id="23d98-112">PARAMETERS</span></span>

### <span data-ttu-id="23d98-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="23d98-113">-Account</span></span>
<span data-ttu-id="23d98-114">要新增計算原則的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="23d98-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="23d98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d98-115">-DefaultProfile</span></span>
<span data-ttu-id="23d98-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="23d98-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23d98-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="23d98-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="23d98-118">此原則每個作業支援的分析單位上限。</span><span class="sxs-lookup"><span data-stu-id="23d98-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="23d98-119">必須指定 this、MinPriorityPerJob 或這兩個參數。</span><span class="sxs-lookup"><span data-stu-id="23d98-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="23d98-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="23d98-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="23d98-121">此原則的每個作業支援的最低優先順序。</span><span class="sxs-lookup"><span data-stu-id="23d98-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="23d98-122">必須指定 this、MaxAnalyticsUnitsPerJob 或這兩個參數。</span><span class="sxs-lookup"><span data-stu-id="23d98-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="23d98-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="23d98-123">-Name</span></span>
<span data-ttu-id="23d98-124">要建立之計算原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="23d98-124">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="23d98-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="23d98-125">-ObjectId</span></span>
<span data-ttu-id="23d98-126">要將原則套用到其中的使用者或群組的 Azure Active Directory 物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="23d98-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d98-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="23d98-127">-ObjectType</span></span>
<span data-ttu-id="23d98-128">傳入之物件識別碼的 Azure Active Directory 物件類型。</span><span class="sxs-lookup"><span data-stu-id="23d98-128">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d98-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23d98-129">-ResourceGroupName</span></span>
<span data-ttu-id="23d98-130">您帳戶所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="23d98-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="23d98-131">[選用]，如果未提供，就會嘗試探索。</span><span class="sxs-lookup"><span data-stu-id="23d98-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="23d98-132">-確認</span><span class="sxs-lookup"><span data-stu-id="23d98-132">-Confirm</span></span>
<span data-ttu-id="23d98-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="23d98-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23d98-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23d98-134">-WhatIf</span></span>
<span data-ttu-id="23d98-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23d98-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23d98-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23d98-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23d98-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d98-137">CommonParameters</span></span>
<span data-ttu-id="23d98-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23d98-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d98-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23d98-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d98-140">輸入</span><span class="sxs-lookup"><span data-stu-id="23d98-140">INPUTS</span></span>

### <span data-ttu-id="23d98-141">System.object</span><span class="sxs-lookup"><span data-stu-id="23d98-141">System.String</span></span>

### <span data-ttu-id="23d98-142">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="23d98-142">System.Guid</span></span>

### <span data-ttu-id="23d98-143">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="23d98-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="23d98-144">輸出</span><span class="sxs-lookup"><span data-stu-id="23d98-144">OUTPUTS</span></span>

### <span data-ttu-id="23d98-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="23d98-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="23d98-146">筆記</span><span class="sxs-lookup"><span data-stu-id="23d98-146">NOTES</span></span>

## <span data-ttu-id="23d98-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="23d98-147">RELATED LINKS</span></span>
