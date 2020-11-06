---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1dfd9c4d55c9898ce9f4b656f53d7606ced11359
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446838"
---
# <span data-ttu-id="5f879-101">New-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="5f879-101">New-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="5f879-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f879-102">SYNOPSIS</span></span>
<span data-ttu-id="5f879-103">建立特定 AAD 實體的資料 Lake Analytics 計算原則規則。</span><span class="sxs-lookup"><span data-stu-id="5f879-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f879-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f879-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f879-105">說明</span><span class="sxs-lookup"><span data-stu-id="5f879-105">DESCRIPTION</span></span>
<span data-ttu-id="5f879-106">**新-AzureRmDataLakeAnalyticsComputePolicy** 會針對 Azure Data Lake Analytics 帳戶中的特定 AAD 實體建立指定的計算原則規則。</span><span class="sxs-lookup"><span data-stu-id="5f879-106">The **New-AzureRmDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="5f879-107">示例</span><span class="sxs-lookup"><span data-stu-id="5f879-107">EXAMPLES</span></span>

### <span data-ttu-id="5f879-108">範例1：建立只有一個規則的計算原則</span><span class="sxs-lookup"><span data-stu-id="5f879-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="5f879-109">這個命令會在帳戶 "contosoadla" 中針對 id 為 "83cb7ad2-3523-4b82-b909-d478b0d8aea3" 的使用者建立名為 "myPolicy" 的原則，以確保他們無法提交超過5個以上並行度的任何作業。</span><span class="sxs-lookup"><span data-stu-id="5f879-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="5f879-110">範例2：建立兩個規則集的計算原則</span><span class="sxs-lookup"><span data-stu-id="5f879-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="5f879-111">這個命令會在帳戶 "contosoadla" 中針對 id 為 "83cb7ad2-3523-4b82-b909-d478b0d8aea3" 的使用者建立名為 "myPolicy" 的原則，以確保他們無法提交超過5個並行度或優先順序低於100的任何作業。</span><span class="sxs-lookup"><span data-stu-id="5f879-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="5f879-112">參數</span><span class="sxs-lookup"><span data-stu-id="5f879-112">PARAMETERS</span></span>

### <span data-ttu-id="5f879-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="5f879-113">-Account</span></span>
<span data-ttu-id="5f879-114">要新增計算原則的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5f879-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="5f879-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="5f879-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="5f879-116">此原則的每個作業支援的最大並行度。</span><span class="sxs-lookup"><span data-stu-id="5f879-116">The maximum supported degree of parallelism per job for this policy.</span></span>
<span data-ttu-id="5f879-117">必須指定 this、MinPriorityPerJob 或這兩個參數。</span><span class="sxs-lookup"><span data-stu-id="5f879-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="5f879-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="5f879-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="5f879-119">此原則的每個作業支援的最低優先順序。</span><span class="sxs-lookup"><span data-stu-id="5f879-119">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="5f879-120">必須指定 this、MaxDegreeOfParallelismPerJob 或這兩個參數。</span><span class="sxs-lookup"><span data-stu-id="5f879-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="5f879-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f879-121">-Name</span></span>
<span data-ttu-id="5f879-122">要建立之計算原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f879-122">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="5f879-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5f879-123">-ObjectId</span></span>
<span data-ttu-id="5f879-124">要將原則套用到其中的使用者或群組的 Azure Active Directory 物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f879-124">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

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

### <span data-ttu-id="5f879-125">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="5f879-125">-ObjectType</span></span>
<span data-ttu-id="5f879-126">傳入之物件識別碼的 Azure Active Directory 物件類型。</span><span class="sxs-lookup"><span data-stu-id="5f879-126">The Azure Active Directory object type for the object ID passed in.</span></span>

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

### <span data-ttu-id="5f879-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f879-127">-ResourceGroupName</span></span>
<span data-ttu-id="5f879-128">您帳戶所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f879-128">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="5f879-129">[選用]，如果未提供，就會嘗試探索。</span><span class="sxs-lookup"><span data-stu-id="5f879-129">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="5f879-130">-確認</span><span class="sxs-lookup"><span data-stu-id="5f879-130">-Confirm</span></span>
<span data-ttu-id="5f879-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5f879-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f879-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f879-132">-WhatIf</span></span>
<span data-ttu-id="5f879-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f879-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f879-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f879-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f879-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f879-135">-DefaultProfile</span></span>
<span data-ttu-id="5f879-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f879-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f879-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f879-137">CommonParameters</span></span>
<span data-ttu-id="5f879-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f879-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f879-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5f879-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f879-140">輸入</span><span class="sxs-lookup"><span data-stu-id="5f879-140">INPUTS</span></span>

### <span data-ttu-id="5f879-141">System.object</span><span class="sxs-lookup"><span data-stu-id="5f879-141">System.String</span></span>
<span data-ttu-id="5f879-142">System.object （即 Guid.empty）</span><span class="sxs-lookup"><span data-stu-id="5f879-142">System.Guid System.Int32</span></span>

## <span data-ttu-id="5f879-143">輸出</span><span class="sxs-lookup"><span data-stu-id="5f879-143">OUTPUTS</span></span>

### <span data-ttu-id="5f879-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="5f879-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="5f879-145">筆記</span><span class="sxs-lookup"><span data-stu-id="5f879-145">NOTES</span></span>

## <span data-ttu-id="5f879-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f879-146">RELATED LINKS</span></span>

