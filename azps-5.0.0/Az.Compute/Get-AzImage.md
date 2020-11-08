---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 4d1de6553a07cf58fdc109dc5703e37392a27a02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140528"
---
# <span data-ttu-id="150c3-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="150c3-101">Get-AzImage</span></span>

## <span data-ttu-id="150c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="150c3-102">SYNOPSIS</span></span>
<span data-ttu-id="150c3-103">取得影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="150c3-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="150c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="150c3-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="150c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="150c3-105">DESCRIPTION</span></span>
<span data-ttu-id="150c3-106">**AzImage** Cmdlet 會取得影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="150c3-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="150c3-107">示例</span><span class="sxs-lookup"><span data-stu-id="150c3-107">EXAMPLES</span></span>

### <span data-ttu-id="150c3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="150c3-108">Example 1</span></span>
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

<span data-ttu-id="150c3-109">這個命令會取得資源群組 ' ResourceGroup01 ' 中名為 ' Image01 ' 的影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="150c3-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="150c3-110">範例2</span><span class="sxs-lookup"><span data-stu-id="150c3-110">Example 2</span></span>
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

<span data-ttu-id="150c3-111">這個命令會取得資源群組 ' ResourceGroup01 ' 中所有影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="150c3-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="150c3-112">範例3</span><span class="sxs-lookup"><span data-stu-id="150c3-112">Example 3</span></span>
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

<span data-ttu-id="150c3-113">這個命令會取得訂閱下所有影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="150c3-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="150c3-114">範例4</span><span class="sxs-lookup"><span data-stu-id="150c3-114">Example 4</span></span>
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

<span data-ttu-id="150c3-115">這個命令會取得以「Image」開頭的訂閱中所有影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="150c3-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="150c3-116">參數</span><span class="sxs-lookup"><span data-stu-id="150c3-116">PARAMETERS</span></span>

### <span data-ttu-id="150c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="150c3-117">-DefaultProfile</span></span>
<span data-ttu-id="150c3-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="150c3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="150c3-119">-展開</span><span class="sxs-lookup"><span data-stu-id="150c3-119">-Expand</span></span>
<span data-ttu-id="150c3-120">指定 [擴大運算式] 查詢。</span><span class="sxs-lookup"><span data-stu-id="150c3-120">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="150c3-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="150c3-121">-ImageName</span></span>
<span data-ttu-id="150c3-122">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="150c3-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="150c3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="150c3-123">-ResourceGroupName</span></span>
<span data-ttu-id="150c3-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="150c3-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="150c3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150c3-125">CommonParameters</span></span>
<span data-ttu-id="150c3-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="150c3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150c3-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="150c3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150c3-128">輸入</span><span class="sxs-lookup"><span data-stu-id="150c3-128">INPUTS</span></span>

### <span data-ttu-id="150c3-129">System.object</span><span class="sxs-lookup"><span data-stu-id="150c3-129">System.String</span></span>

## <span data-ttu-id="150c3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="150c3-130">OUTPUTS</span></span>

### <span data-ttu-id="150c3-131">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="150c3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="150c3-132">筆記</span><span class="sxs-lookup"><span data-stu-id="150c3-132">NOTES</span></span>

## <span data-ttu-id="150c3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="150c3-133">RELATED LINKS</span></span>
