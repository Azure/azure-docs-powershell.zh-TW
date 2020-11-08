---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 7e10c24c62a05650fd618793cb8de088237357ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969788"
---
# <span data-ttu-id="d4a4a-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="d4a4a-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="d4a4a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a4a-103">取得 Azure 資料共用中資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d4a4a-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="d4a4a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4a4a-104">SYNTAX</span></span>

### <span data-ttu-id="d4a4a-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d4a4a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4a4a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a4a-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4a4a-107">說明</span><span class="sxs-lookup"><span data-stu-id="d4a4a-107">DESCRIPTION</span></span>
<span data-ttu-id="d4a4a-108">**AzDataShareDataSet** Cmdlet 會取得在 Azure 資料共用帳戶的共用中新增資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d4a4a-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="d4a4a-109">如果您指定資料集的名稱，此 Cmdlet 會取得資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d4a4a-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="d4a4a-110">如果您沒有指定名稱，此 Cmdlet 會取得共用中所有資料集的相關資訊。是否</span><span class="sxs-lookup"><span data-stu-id="d4a4a-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="d4a4a-111">示例</span><span class="sxs-lookup"><span data-stu-id="d4a4a-111">EXAMPLES</span></span>

### <span data-ttu-id="d4a4a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="d4a4a-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="d4a4a-113">這個命令會在 Azure 資料共用帳戶 WikiAdsAccount 和資源群組廣告的共用 AdsShare 中，顯示資料集 AdsDataSet 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d4a4a-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="d4a4a-114">參數</span><span class="sxs-lookup"><span data-stu-id="d4a4a-114">PARAMETERS</span></span>

### <span data-ttu-id="d4a4a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d4a4a-115">-AccountName</span></span>
<span data-ttu-id="d4a4a-116">Azure 資料共用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a4a-116">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a4a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a4a-117">-DefaultProfile</span></span>
<span data-ttu-id="d4a4a-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4a4a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4a4a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4a4a-119">-Name</span></span>
<span data-ttu-id="d4a4a-120">Azure 資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a4a-120">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a4a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a4a-121">-ResourceGroupName</span></span>
<span data-ttu-id="d4a4a-122">Azure 資料共用帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a4a-122">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a4a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4a4a-123">-ResourceId</span></span>
<span data-ttu-id="d4a4a-124">Azure 資料集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4a4a-124">The resource id of the azure data set.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4a4a-125">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="d4a4a-125">-ShareName</span></span>
<span data-ttu-id="d4a4a-126">Azure 資料共用名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a4a-126">Azure data share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a4a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a4a-127">CommonParameters</span></span>
<span data-ttu-id="d4a4a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4a4a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a4a-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d4a4a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a4a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d4a4a-130">INPUTS</span></span>

### <span data-ttu-id="d4a4a-131">System.object</span><span class="sxs-lookup"><span data-stu-id="d4a4a-131">System.String</span></span>

## <span data-ttu-id="d4a4a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d4a4a-132">OUTPUTS</span></span>

### <span data-ttu-id="d4a4a-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="d4a4a-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="d4a4a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d4a4a-134">NOTES</span></span>

## <span data-ttu-id="d4a4a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4a4a-135">RELATED LINKS</span></span>
