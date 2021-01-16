---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: 99f80aa920a402867b6385a3b4ef7ac118838f80
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280056"
---
# <span data-ttu-id="c4f8c-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="c4f8c-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="c4f8c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4f8c-102">SYNOPSIS</span></span>
<span data-ttu-id="c4f8c-103">取得共用訂閱中資料集映射的相關資訊</span><span class="sxs-lookup"><span data-stu-id="c4f8c-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="c4f8c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4f8c-104">SYNTAX</span></span>

### <span data-ttu-id="c4f8c-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c4f8c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4f8c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4f8c-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4f8c-107">說明</span><span class="sxs-lookup"><span data-stu-id="c4f8c-107">DESCRIPTION</span></span>
<span data-ttu-id="c4f8c-108">如果指定名稱，則 **AzDataShareDataSetMapping** Cmdlet 會取得特定資料集對應的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="c4f8c-109">否則，它會取得共用訂閱中所有資料集對應的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="c4f8c-110">示例</span><span class="sxs-lookup"><span data-stu-id="c4f8c-110">EXAMPLES</span></span>

### <span data-ttu-id="c4f8c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c4f8c-111">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareSubscriptionName "WikiADS"

ContainerName        : testing
Prefix               : providercontainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : storageaccount
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/WikiADS/dataSetMappings/dsm
Name                 : dsm
Type                 : Microsoft.DataShare/DataSetMappings
```

 <span data-ttu-id="c4f8c-112">這個命令會顯示共用訂閱中所有資料集映射的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="c4f8c-113">參數</span><span class="sxs-lookup"><span data-stu-id="c4f8c-113">PARAMETERS</span></span>

### <span data-ttu-id="c4f8c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c4f8c-114">-AccountName</span></span>
<span data-ttu-id="c4f8c-115">Azure 資料共用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="c4f8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4f8c-116">-DefaultProfile</span></span>
<span data-ttu-id="c4f8c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4f8c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c4f8c-118">-Name</span></span>
<span data-ttu-id="c4f8c-119">Azure 資料集對應名稱。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="c4f8c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4f8c-120">-ResourceGroupName</span></span>
<span data-ttu-id="c4f8c-121">Azure 資料共用帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="c4f8c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4f8c-122">-ResourceId</span></span>
<span data-ttu-id="c4f8c-123">Azure 資料集對應的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="c4f8c-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c4f8c-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="c4f8c-125">Azure 資料共用訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="c4f8c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4f8c-126">CommonParameters</span></span>
<span data-ttu-id="c4f8c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4f8c-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4f8c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c4f8c-129">INPUTS</span></span>

### <span data-ttu-id="c4f8c-130">System.object</span><span class="sxs-lookup"><span data-stu-id="c4f8c-130">System.String</span></span>

## <span data-ttu-id="c4f8c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="c4f8c-131">OUTPUTS</span></span>

### <span data-ttu-id="c4f8c-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="c4f8c-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="c4f8c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="c4f8c-133">NOTES</span></span>

## <span data-ttu-id="c4f8c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4f8c-134">RELATED LINKS</span></span>
