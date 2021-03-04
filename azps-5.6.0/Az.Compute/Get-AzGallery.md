---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: 7764ee4cd151e3de7cca2af84ed0cf670c52a6a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906245"
---
# <span data-ttu-id="d4d46-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="d4d46-101">Get-AzGallery</span></span>

## <span data-ttu-id="d4d46-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d4d46-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d46-103">取得或清單庫。</span><span class="sxs-lookup"><span data-stu-id="d4d46-103">Get or list galleries.</span></span>

## <span data-ttu-id="d4d46-104">語法</span><span class="sxs-lookup"><span data-stu-id="d4d46-104">SYNTAX</span></span>

### <span data-ttu-id="d4d46-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="d4d46-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4d46-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d4d46-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4d46-107">描述</span><span class="sxs-lookup"><span data-stu-id="d4d46-107">DESCRIPTION</span></span>
<span data-ttu-id="d4d46-108">取得或清單庫。</span><span class="sxs-lookup"><span data-stu-id="d4d46-108">Get or list galleries.</span></span>

## <span data-ttu-id="d4d46-109">例子</span><span class="sxs-lookup"><span data-stu-id="d4d46-109">EXAMPLES</span></span>

### <span data-ttu-id="d4d46-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="d4d46-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="d4d46-111">取得圖庫 "gallery1"</span><span class="sxs-lookup"><span data-stu-id="d4d46-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="d4d46-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="d4d46-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="d4d46-113">取得 rg1 的所有圖庫。</span><span class="sxs-lookup"><span data-stu-id="d4d46-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="d4d46-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="d4d46-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGallery

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="d4d46-115">取得訂閱中所有的圖庫。</span><span class="sxs-lookup"><span data-stu-id="d4d46-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="d4d46-116">範例 4</span><span class="sxs-lookup"><span data-stu-id="d4d46-116">Example 4</span></span>
```powershell
PS C:\> Get-AzGallery -Name gallery*

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="d4d46-117">取得訂閱中以「圖庫」為起點的所有圖庫。</span><span class="sxs-lookup"><span data-stu-id="d4d46-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="d4d46-118">參數</span><span class="sxs-lookup"><span data-stu-id="d4d46-118">PARAMETERS</span></span>

### <span data-ttu-id="d4d46-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d46-119">-DefaultProfile</span></span>
<span data-ttu-id="d4d46-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4d46-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4d46-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4d46-121">-Name</span></span>
<span data-ttu-id="d4d46-122">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4d46-122">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d4d46-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4d46-123">-ResourceGroupName</span></span>
<span data-ttu-id="d4d46-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4d46-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d4d46-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4d46-125">-ResourceId</span></span>
<span data-ttu-id="d4d46-126">圖庫的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d4d46-126">The resource id for Gallery</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d46-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d46-127">CommonParameters</span></span>
<span data-ttu-id="d4d46-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d4d46-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d46-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4d46-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d46-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d4d46-130">INPUTS</span></span>

### <span data-ttu-id="d4d46-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d4d46-131">System.String</span></span>

## <span data-ttu-id="d4d46-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d4d46-132">OUTPUTS</span></span>

### <span data-ttu-id="d4d46-133">Microsoft.Azure.Commands.Compute.Automation.models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="d4d46-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="d4d46-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d4d46-134">NOTES</span></span>

## <span data-ttu-id="d4d46-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4d46-135">RELATED LINKS</span></span>
