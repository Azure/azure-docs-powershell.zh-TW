---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: d0bf60bbfd13474270391afd6f01bc9ec8130b62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912021"
---
# <span data-ttu-id="ed1f5-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="ed1f5-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="ed1f5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ed1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ed1f5-103">在 Azure 資料共用中，獲得資料集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ed1f5-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="ed1f5-104">語法</span><span class="sxs-lookup"><span data-stu-id="ed1f5-104">SYNTAX</span></span>

### <span data-ttu-id="ed1f5-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ed1f5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed1f5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed1f5-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed1f5-107">描述</span><span class="sxs-lookup"><span data-stu-id="ed1f5-107">DESCRIPTION</span></span>
<span data-ttu-id="ed1f5-108">**Get-AzDataShareDataSet** Cmdlet 會取得在 Azure 資料共用帳戶中共用新增的資料集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ed1f5-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="ed1f5-109">如果您指定資料集的名稱，此 Cmdlet 會獲得資料集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ed1f5-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="ed1f5-110">如果您未指定名稱，此 Cmdlet 會獲得共用中所有資料集的資訊。Ⅰ</span><span class="sxs-lookup"><span data-stu-id="ed1f5-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="ed1f5-111">例子</span><span class="sxs-lookup"><span data-stu-id="ed1f5-111">EXAMPLES</span></span>

### <span data-ttu-id="ed1f5-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="ed1f5-112">Example 1</span></span>
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

<span data-ttu-id="ed1f5-113">此命令會顯示 Azure 資料共用帳戶 WikiAdsAccount和資源群組 ADS 中的 AdsDataSet 資料集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ed1f5-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="ed1f5-114">參數</span><span class="sxs-lookup"><span data-stu-id="ed1f5-114">PARAMETERS</span></span>

### <span data-ttu-id="ed1f5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed1f5-115">-AccountName</span></span>
<span data-ttu-id="ed1f5-116">Azure 資料共用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ed1f5-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="ed1f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed1f5-117">-DefaultProfile</span></span>
<span data-ttu-id="ed1f5-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed1f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed1f5-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed1f5-119">-Name</span></span>
<span data-ttu-id="ed1f5-120">Azure 資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="ed1f5-120">Azure data set name.</span></span>

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

### <span data-ttu-id="ed1f5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed1f5-121">-ResourceGroupName</span></span>
<span data-ttu-id="ed1f5-122">Azure 資料共用帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ed1f5-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="ed1f5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed1f5-123">-ResourceId</span></span>
<span data-ttu-id="ed1f5-124">Azure 資料集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed1f5-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="ed1f5-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ed1f5-125">-ShareName</span></span>
<span data-ttu-id="ed1f5-126">Azure 資料共用名稱。</span><span class="sxs-lookup"><span data-stu-id="ed1f5-126">Azure data share name.</span></span>

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

### <span data-ttu-id="ed1f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed1f5-127">CommonParameters</span></span>
<span data-ttu-id="ed1f5-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ed1f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed1f5-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed1f5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed1f5-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ed1f5-130">INPUTS</span></span>

### <span data-ttu-id="ed1f5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ed1f5-131">System.String</span></span>

## <span data-ttu-id="ed1f5-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ed1f5-132">OUTPUTS</span></span>

### <span data-ttu-id="ed1f5-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="ed1f5-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="ed1f5-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ed1f5-134">NOTES</span></span>

## <span data-ttu-id="ed1f5-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed1f5-135">RELATED LINKS</span></span>
