---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
ms.openlocfilehash: bff748b8c867b272208469d34229cc2724bc8610
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447440"
---
# <span data-ttu-id="30a85-101">Get-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="30a85-101">Get-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="30a85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30a85-102">SYNOPSIS</span></span>
<span data-ttu-id="30a85-103">[取得] 或 [清單庫] 影像版本。</span><span class="sxs-lookup"><span data-stu-id="30a85-103">Get or list gallery image versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30a85-104">句法</span><span class="sxs-lookup"><span data-stu-id="30a85-104">SYNTAX</span></span>

### <span data-ttu-id="30a85-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="30a85-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30a85-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="30a85-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30a85-107">說明</span><span class="sxs-lookup"><span data-stu-id="30a85-107">DESCRIPTION</span></span>
<span data-ttu-id="30a85-108">[取得] 或 [清單庫] 影像版本。</span><span class="sxs-lookup"><span data-stu-id="30a85-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="30a85-109">示例</span><span class="sxs-lookup"><span data-stu-id="30a85-109">EXAMPLES</span></span>

### <span data-ttu-id="30a85-110">範例1</span><span class="sxs-lookup"><span data-stu-id="30a85-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="30a85-111">取得圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="30a85-111">Get the gallery image version.</span></span>

## <span data-ttu-id="30a85-112">參數</span><span class="sxs-lookup"><span data-stu-id="30a85-112">PARAMETERS</span></span>

### <span data-ttu-id="30a85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a85-113">-DefaultProfile</span></span>
<span data-ttu-id="30a85-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30a85-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30a85-115">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="30a85-115">-ExpandReplicationStatus</span></span>
<span data-ttu-id="30a85-116">顯示覆制狀態。</span><span class="sxs-lookup"><span data-stu-id="30a85-116">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30a85-117">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="30a85-117">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="30a85-118">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="30a85-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30a85-119">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="30a85-119">-GalleryName</span></span>
<span data-ttu-id="30a85-120">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="30a85-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30a85-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="30a85-121">-Name</span></span>
<span data-ttu-id="30a85-122">圖庫影像版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="30a85-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30a85-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30a85-123">-ResourceGroupName</span></span>
<span data-ttu-id="30a85-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="30a85-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30a85-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30a85-125">-ResourceId</span></span>
<span data-ttu-id="30a85-126">畫廊影像版本的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="30a85-126">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="30a85-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a85-127">CommonParameters</span></span>
<span data-ttu-id="30a85-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30a85-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a85-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30a85-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a85-130">輸入</span><span class="sxs-lookup"><span data-stu-id="30a85-130">INPUTS</span></span>

### <span data-ttu-id="30a85-131">System.object</span><span class="sxs-lookup"><span data-stu-id="30a85-131">System.String</span></span>

### <span data-ttu-id="30a85-132">PSGalleryImageVersion 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="30a85-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="30a85-133">輸出</span><span class="sxs-lookup"><span data-stu-id="30a85-133">OUTPUTS</span></span>

### <span data-ttu-id="30a85-134">PSGalleryImageVersion 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="30a85-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="30a85-135">筆記</span><span class="sxs-lookup"><span data-stu-id="30a85-135">NOTES</span></span>

## <span data-ttu-id="30a85-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="30a85-136">RELATED LINKS</span></span>
