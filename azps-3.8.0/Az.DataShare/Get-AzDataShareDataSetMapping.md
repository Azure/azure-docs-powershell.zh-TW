---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: cf8b235d0035955f809b167ba4d532cdae0538c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956655"
---
# <span data-ttu-id="3f9b8-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="3f9b8-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="3f9b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f9b8-102">SYNOPSIS</span></span>
<span data-ttu-id="3f9b8-103">取得共用訂閱中資料集映射的相關資訊</span><span class="sxs-lookup"><span data-stu-id="3f9b8-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="3f9b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f9b8-104">SYNTAX</span></span>

### <span data-ttu-id="3f9b8-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3f9b8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f9b8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f9b8-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f9b8-107">說明</span><span class="sxs-lookup"><span data-stu-id="3f9b8-107">DESCRIPTION</span></span>
<span data-ttu-id="3f9b8-108">如果指定名稱，則 **AzDataShareDataSetMapping** Cmdlet 會取得特定資料集對應的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3f9b8-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="3f9b8-109">否則，它會取得共用訂閱中所有資料集對應的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3f9b8-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="3f9b8-110">示例</span><span class="sxs-lookup"><span data-stu-id="3f9b8-110">EXAMPLES</span></span>

### <span data-ttu-id="3f9b8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3f9b8-111">Example 1</span></span>
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

 <span data-ttu-id="3f9b8-112">這個命令會顯示共用訂閱中所有資料集映射的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3f9b8-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="3f9b8-113">參數</span><span class="sxs-lookup"><span data-stu-id="3f9b8-113">PARAMETERS</span></span>

### <span data-ttu-id="3f9b8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3f9b8-114">-AccountName</span></span>
<span data-ttu-id="3f9b8-115">Azure 資料共用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3f9b8-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="3f9b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f9b8-116">-DefaultProfile</span></span>
<span data-ttu-id="3f9b8-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f9b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f9b8-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="3f9b8-118">-Name</span></span>
<span data-ttu-id="3f9b8-119">Azure 資料集對應名稱。</span><span class="sxs-lookup"><span data-stu-id="3f9b8-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="3f9b8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f9b8-120">-ResourceGroupName</span></span>
<span data-ttu-id="3f9b8-121">Azure 資料共用帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3f9b8-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="3f9b8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f9b8-122">-ResourceId</span></span>
<span data-ttu-id="3f9b8-123">Azure 資料集對應的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f9b8-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="3f9b8-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3f9b8-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="3f9b8-125">Azure 資料共用訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="3f9b8-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="3f9b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f9b8-126">CommonParameters</span></span>
<span data-ttu-id="3f9b8-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f9b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f9b8-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f9b8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f9b8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3f9b8-129">INPUTS</span></span>

### <span data-ttu-id="3f9b8-130">System.object</span><span class="sxs-lookup"><span data-stu-id="3f9b8-130">System.String</span></span>

## <span data-ttu-id="3f9b8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3f9b8-131">OUTPUTS</span></span>

### <span data-ttu-id="3f9b8-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="3f9b8-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="3f9b8-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3f9b8-133">NOTES</span></span>

## <span data-ttu-id="3f9b8-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f9b8-134">RELATED LINKS</span></span>
