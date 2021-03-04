---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 8261a4ee59d7a29911e7cfde3b28b5d28e3e1ae5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906234"
---
# <span data-ttu-id="3775b-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="3775b-101">Get-AzImage</span></span>

## <span data-ttu-id="3775b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3775b-102">SYNOPSIS</span></span>
<span data-ttu-id="3775b-103">獲得影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="3775b-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="3775b-104">語法</span><span class="sxs-lookup"><span data-stu-id="3775b-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3775b-105">描述</span><span class="sxs-lookup"><span data-stu-id="3775b-105">DESCRIPTION</span></span>
<span data-ttu-id="3775b-106">**Get-AzImage** Cmdlet 會取得影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="3775b-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="3775b-107">例子</span><span class="sxs-lookup"><span data-stu-id="3775b-107">EXAMPLES</span></span>

### <span data-ttu-id="3775b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="3775b-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="3775b-109">此命令會獲得資源群組 "ResourceGroup01" 中名為 "Image01" 的影像屬性。</span><span class="sxs-lookup"><span data-stu-id="3775b-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="3775b-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="3775b-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="3775b-111">此命令會獲得資源群組 "ResourceGroup01" 中所有圖像的屬性。</span><span class="sxs-lookup"><span data-stu-id="3775b-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="3775b-112">範例 3</span><span class="sxs-lookup"><span data-stu-id="3775b-112">Example 3</span></span>
```
PS C:\> Get-AzImage

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="3775b-113">此命令會獲得訂閱下所有影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="3775b-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="3775b-114">範例 4</span><span class="sxs-lookup"><span data-stu-id="3775b-114">Example 4</span></span>
```
PS C:\> Get-AzImage -Name "Image*"

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="3775b-115">此命令會獲得訂閱下以「影像」為起始之所有影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="3775b-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="3775b-116">參數</span><span class="sxs-lookup"><span data-stu-id="3775b-116">PARAMETERS</span></span>

### <span data-ttu-id="3775b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3775b-117">-DefaultProfile</span></span>
<span data-ttu-id="3775b-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3775b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3775b-119">-展開</span><span class="sxs-lookup"><span data-stu-id="3775b-119">-Expand</span></span>
<span data-ttu-id="3775b-120">指定展開運算式查詢。</span><span class="sxs-lookup"><span data-stu-id="3775b-120">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3775b-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="3775b-121">-ImageName</span></span>
<span data-ttu-id="3775b-122">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="3775b-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3775b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3775b-123">-ResourceGroupName</span></span>
<span data-ttu-id="3775b-124">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3775b-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3775b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3775b-125">CommonParameters</span></span>
<span data-ttu-id="3775b-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3775b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3775b-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3775b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3775b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="3775b-128">INPUTS</span></span>

### <span data-ttu-id="3775b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3775b-129">System.String</span></span>

## <span data-ttu-id="3775b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3775b-130">OUTPUTS</span></span>

### <span data-ttu-id="3775b-131">Microsoft.Azure.Commands.Compute.Automation.models.PSImage</span><span class="sxs-lookup"><span data-stu-id="3775b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="3775b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3775b-132">NOTES</span></span>

## <span data-ttu-id="3775b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="3775b-133">RELATED LINKS</span></span>
