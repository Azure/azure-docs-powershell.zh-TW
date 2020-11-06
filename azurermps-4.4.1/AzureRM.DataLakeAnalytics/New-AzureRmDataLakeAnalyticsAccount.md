---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 7c35821cbaf75a616ab1b9b8bbc2db9fc2a96794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455835"
---
# <span data-ttu-id="4f3f3-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4f3f3-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="4f3f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="4f3f3-103">建立資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f3f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f3f3-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tags] <Hashtable>] [-MaxDegreeOfParallelism <Int32>]
 [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f3f3-105">說明</span><span class="sxs-lookup"><span data-stu-id="4f3f3-105">DESCRIPTION</span></span>
<span data-ttu-id="4f3f3-106">**新的-AzureRmDataLakeAnalyticsAccount** Cmdlet 會建立 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4f3f3-107">示例</span><span class="sxs-lookup"><span data-stu-id="4f3f3-107">EXAMPLES</span></span>

### <span data-ttu-id="4f3f3-108">範例1：建立資料 Lake Analytics 帳戶</span><span class="sxs-lookup"><span data-stu-id="4f3f3-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="4f3f3-109">這個命令會在名為 ContosoOrg 的資源群組中，建立一個名為 ContosoAdlAccount 的資料 Lake Analytics 帳戶，該帳戶會使用 ContosoAdlStore 資料存放區。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="4f3f3-110">參數</span><span class="sxs-lookup"><span data-stu-id="4f3f3-110">PARAMETERS</span></span>

### <span data-ttu-id="4f3f3-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4f3f3-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="4f3f3-112">指定要設定為預設資料來源的 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3f3-113">-位置</span><span class="sxs-lookup"><span data-stu-id="4f3f3-113">-Location</span></span>
<span data-ttu-id="4f3f3-114">指定建立資料 Lake Analytics 帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-114">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="4f3f3-115">目前僅支援東美國2。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-115">Only East US 2 is supported at this time.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3f3-116">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="4f3f3-116">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="4f3f3-117">此帳戶所支援的選用最大並行度。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-117">The optional maximum supported degree of parallelism for this account.</span></span> <span data-ttu-id="4f3f3-118">如果沒有指定，則預設為30</span><span class="sxs-lookup"><span data-stu-id="4f3f3-118">If none is specified, defaults to 30</span></span>

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

### <span data-ttu-id="4f3f3-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="4f3f3-119">-MaxJobCount</span></span>
<span data-ttu-id="4f3f3-120">同時在帳戶下執行的選用最大作業數。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-120">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="4f3f3-121">如果沒有指定，則預設為3</span><span class="sxs-lookup"><span data-stu-id="4f3f3-121">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="4f3f3-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f3f3-122">-Name</span></span>
<span data-ttu-id="4f3f3-123">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-123">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3f3-124">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="4f3f3-124">-QueryStoreRetention</span></span>
<span data-ttu-id="4f3f3-125">保留作業中繼資料的可選天數。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-125">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="4f3f3-126">如果沒有指定，則預設值為30天。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-126">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="4f3f3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f3f3-127">-ResourceGroupName</span></span>
<span data-ttu-id="4f3f3-128">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-128">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="4f3f3-129">若要建立資源群組，請使用 New-AzureRmResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-129">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3f3-130">-標記</span><span class="sxs-lookup"><span data-stu-id="4f3f3-130">-Tags</span></span>
<span data-ttu-id="4f3f3-131">指定可用於在其他 Azure 資源之間識別資料 Lake Analytics 帳戶的鍵值對。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-131">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3f3-132">層級</span><span class="sxs-lookup"><span data-stu-id="4f3f3-132">-Tier</span></span>
<span data-ttu-id="4f3f3-133">此帳戶要使用的預期承諾層級。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-133">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases: 
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3f3-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f3f3-134">-DefaultProfile</span></span>
<span data-ttu-id="4f3f3-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f3f3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f3f3-136">CommonParameters</span></span>
<span data-ttu-id="4f3f3-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f3f3-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f3f3-139">輸入</span><span class="sxs-lookup"><span data-stu-id="4f3f3-139">INPUTS</span></span>

## <span data-ttu-id="4f3f3-140">輸出</span><span class="sxs-lookup"><span data-stu-id="4f3f3-140">OUTPUTS</span></span>

### <span data-ttu-id="4f3f3-141">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4f3f3-141">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="4f3f3-142">新建立的帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4f3f3-142">The details of the newly created account.</span></span>

## <span data-ttu-id="4f3f3-143">筆記</span><span class="sxs-lookup"><span data-stu-id="4f3f3-143">NOTES</span></span>

## <span data-ttu-id="4f3f3-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f3f3-144">RELATED LINKS</span></span>

[<span data-ttu-id="4f3f3-145">AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4f3f3-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4f3f3-146">移除-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4f3f3-146">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4f3f3-147">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4f3f3-147">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4f3f3-148">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4f3f3-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


