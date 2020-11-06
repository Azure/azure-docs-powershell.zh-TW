---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 36bf1bbfeb0c44189f5eeeaa0988d0314980e48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447833"
---
# <span data-ttu-id="837ce-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="837ce-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="837ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="837ce-102">SYNOPSIS</span></span>
<span data-ttu-id="837ce-103">建立資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="837ce-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="837ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="837ce-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="837ce-105">說明</span><span class="sxs-lookup"><span data-stu-id="837ce-105">DESCRIPTION</span></span>
<span data-ttu-id="837ce-106">**新的-AzureRmDataLakeAnalyticsAccount** Cmdlet 會建立 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="837ce-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="837ce-107">示例</span><span class="sxs-lookup"><span data-stu-id="837ce-107">EXAMPLES</span></span>

### <span data-ttu-id="837ce-108">範例1：建立資料 Lake Analytics 帳戶</span><span class="sxs-lookup"><span data-stu-id="837ce-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="837ce-109">這個命令會在名為 ContosoOrg 的資源群組中，建立一個名為 ContosoAdlAccount 的資料 Lake Analytics 帳戶，該帳戶會使用 ContosoAdlStore 資料存放區。</span><span class="sxs-lookup"><span data-stu-id="837ce-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="837ce-110">參數</span><span class="sxs-lookup"><span data-stu-id="837ce-110">PARAMETERS</span></span>

### <span data-ttu-id="837ce-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="837ce-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="837ce-112">指定要設定為預設資料來源的 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="837ce-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="837ce-113">-DefaultProfile</span></span>
<span data-ttu-id="837ce-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="837ce-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837ce-115">-位置</span><span class="sxs-lookup"><span data-stu-id="837ce-115">-Location</span></span>
<span data-ttu-id="837ce-116">指定建立資料 Lake Analytics 帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="837ce-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="837ce-117">目前僅支援東美國2。</span><span class="sxs-lookup"><span data-stu-id="837ce-117">Only East US 2 is supported at this time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837ce-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="837ce-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="837ce-119">此帳戶的選用最大支援分析單位。</span><span class="sxs-lookup"><span data-stu-id="837ce-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837ce-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="837ce-120">-MaxJobCount</span></span>
<span data-ttu-id="837ce-121">同時在帳戶下執行的選用最大作業數。</span><span class="sxs-lookup"><span data-stu-id="837ce-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="837ce-122">如果沒有指定，則預設為3</span><span class="sxs-lookup"><span data-stu-id="837ce-122">If none is specified, defaults to 3</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837ce-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="837ce-123">-Name</span></span>
<span data-ttu-id="837ce-124">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="837ce-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837ce-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="837ce-125">-QueryStoreRetention</span></span>
<span data-ttu-id="837ce-126">保留作業中繼資料的可選天數。</span><span class="sxs-lookup"><span data-stu-id="837ce-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="837ce-127">如果沒有指定，則預設值為30天。</span><span class="sxs-lookup"><span data-stu-id="837ce-127">If none specified, the default is 30 days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837ce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="837ce-128">-ResourceGroupName</span></span>
<span data-ttu-id="837ce-129">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="837ce-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="837ce-130">若要建立資源群組，請使用 New-AzureRmResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="837ce-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837ce-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="837ce-131">-Tag</span></span>
<span data-ttu-id="837ce-132">與此帳戶相關聯之標記的字串字典</span><span class="sxs-lookup"><span data-stu-id="837ce-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837ce-133">層級</span><span class="sxs-lookup"><span data-stu-id="837ce-133">-Tier</span></span>
<span data-ttu-id="837ce-134">此帳戶要使用的預期承諾層級。</span><span class="sxs-lookup"><span data-stu-id="837ce-134">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837ce-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="837ce-135">CommonParameters</span></span>
<span data-ttu-id="837ce-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="837ce-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="837ce-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="837ce-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="837ce-138">輸入</span><span class="sxs-lookup"><span data-stu-id="837ce-138">INPUTS</span></span>

### <span data-ttu-id="837ce-139">所有</span><span class="sxs-lookup"><span data-stu-id="837ce-139">None</span></span>
<span data-ttu-id="837ce-140">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="837ce-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="837ce-141">輸出</span><span class="sxs-lookup"><span data-stu-id="837ce-141">OUTPUTS</span></span>

### <span data-ttu-id="837ce-142">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="837ce-142">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="837ce-143">新建立的帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="837ce-143">The details of the newly created account.</span></span>

## <span data-ttu-id="837ce-144">筆記</span><span class="sxs-lookup"><span data-stu-id="837ce-144">NOTES</span></span>

## <span data-ttu-id="837ce-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="837ce-145">RELATED LINKS</span></span>

[<span data-ttu-id="837ce-146">AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="837ce-146">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="837ce-147">移除-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="837ce-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="837ce-148">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="837ce-148">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="837ce-149">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="837ce-149">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


