---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
ms.openlocfilehash: cdb703144daa6f9abd62aee41eaad94b2cfa50e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447448"
---
# <span data-ttu-id="93067-101">Get-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="93067-101">Get-AzureRmGallery</span></span>

## <span data-ttu-id="93067-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93067-102">SYNOPSIS</span></span>
<span data-ttu-id="93067-103">[取得] 或 [清單] 樣式庫。</span><span class="sxs-lookup"><span data-stu-id="93067-103">Get or list galleries.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93067-104">句法</span><span class="sxs-lookup"><span data-stu-id="93067-104">SYNTAX</span></span>

### <span data-ttu-id="93067-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="93067-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGallery [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93067-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="93067-106">ResourceIdParameter</span></span>
```
Get-AzureRmGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93067-107">說明</span><span class="sxs-lookup"><span data-stu-id="93067-107">DESCRIPTION</span></span>
<span data-ttu-id="93067-108">[取得] 或 [清單] 樣式庫。</span><span class="sxs-lookup"><span data-stu-id="93067-108">Get or list galleries.</span></span>

## <span data-ttu-id="93067-109">示例</span><span class="sxs-lookup"><span data-stu-id="93067-109">EXAMPLES</span></span>

### <span data-ttu-id="93067-110">範例1</span><span class="sxs-lookup"><span data-stu-id="93067-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGallery -ResourceGroupName $rgname -GalleryName $galleryName

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

<span data-ttu-id="93067-111">取得圖庫。</span><span class="sxs-lookup"><span data-stu-id="93067-111">Get the gallery.</span></span>

## <span data-ttu-id="93067-112">參數</span><span class="sxs-lookup"><span data-stu-id="93067-112">PARAMETERS</span></span>

### <span data-ttu-id="93067-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93067-113">-DefaultProfile</span></span>
<span data-ttu-id="93067-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93067-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93067-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="93067-115">-Name</span></span>
<span data-ttu-id="93067-116">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="93067-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93067-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93067-117">-ResourceGroupName</span></span>
<span data-ttu-id="93067-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="93067-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93067-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93067-119">-ResourceId</span></span>
<span data-ttu-id="93067-120">圖庫的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="93067-120">The resource id for Gallery</span></span>

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

### <span data-ttu-id="93067-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93067-121">CommonParameters</span></span>
<span data-ttu-id="93067-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93067-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93067-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="93067-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93067-124">輸入</span><span class="sxs-lookup"><span data-stu-id="93067-124">INPUTS</span></span>

### <span data-ttu-id="93067-125">System.object</span><span class="sxs-lookup"><span data-stu-id="93067-125">System.String</span></span>

### <span data-ttu-id="93067-126">PSGallery 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="93067-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="93067-127">輸出</span><span class="sxs-lookup"><span data-stu-id="93067-127">OUTPUTS</span></span>

### <span data-ttu-id="93067-128">PSGallery 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="93067-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="93067-129">筆記</span><span class="sxs-lookup"><span data-stu-id="93067-129">NOTES</span></span>

## <span data-ttu-id="93067-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="93067-130">RELATED LINKS</span></span>
