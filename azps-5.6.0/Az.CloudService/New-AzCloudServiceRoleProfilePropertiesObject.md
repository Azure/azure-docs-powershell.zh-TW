---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceRoleProfilePropertiesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
ms.openlocfilehash: 6eec8f849d555fd2bf71f564c2e5c3ed9c699d80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908622"
---
# <span data-ttu-id="6c3e6-101">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="6c3e6-101">New-AzCloudServiceRoleProfilePropertiesObject</span></span>

## <span data-ttu-id="6c3e6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6c3e6-102">SYNOPSIS</span></span>
<span data-ttu-id="6c3e6-103">為 CloudServiceRoleProfileProperties 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="6c3e6-103">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="6c3e6-104">語法</span><span class="sxs-lookup"><span data-stu-id="6c3e6-104">SYNTAX</span></span>

```
New-AzCloudServiceRoleProfilePropertiesObject [-Name <String>] [-SkuCapacity <Int64>] [-SkuName <String>]
 [-SkuTier <String>] [<CommonParameters>]
```

## <span data-ttu-id="6c3e6-105">描述</span><span class="sxs-lookup"><span data-stu-id="6c3e6-105">DESCRIPTION</span></span>
<span data-ttu-id="6c3e6-106">為 CloudServiceRoleProfileProperties 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="6c3e6-106">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="6c3e6-107">例子</span><span class="sxs-lookup"><span data-stu-id="6c3e6-107">EXAMPLES</span></span>

### <span data-ttu-id="6c3e6-108">範例 1：建立角色配置檔案屬性物件</span><span class="sxs-lookup"><span data-stu-id="6c3e6-108">Example 1: Create role profile properties object</span></span>
```powershell
$role = New-AzCloudServiceRoleProfilePropertiesObject -Name 'WebRole' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
```

<span data-ttu-id="6c3e6-109">此命令會建立角色配置檔案屬性物件，用於建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-109">This command creates role profile properties object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="6c3e6-110">詳情請參閱 New-AzCloudService。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="6c3e6-111">參數</span><span class="sxs-lookup"><span data-stu-id="6c3e6-111">PARAMETERS</span></span>

### <span data-ttu-id="6c3e6-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c3e6-112">-Name</span></span>
<span data-ttu-id="6c3e6-113">角色設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-113">Name of role profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c3e6-114">-Sku以</span><span class="sxs-lookup"><span data-stu-id="6c3e6-114">-SkuCapacity</span></span>
<span data-ttu-id="6c3e6-115">指定雲端服務中的角色實例數目。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-115">Specifies the number of role instances in the cloud service.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c3e6-116">-SKUName</span><span class="sxs-lookup"><span data-stu-id="6c3e6-116">-SkuName</span></span>
<span data-ttu-id="6c3e6-117">SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-117">The sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c3e6-118">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6c3e6-118">-SkuTier</span></span>
<span data-ttu-id="6c3e6-119">SkuTier。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-119">SkuTier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c3e6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c3e6-120">CommonParameters</span></span>
<span data-ttu-id="6c3e6-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6c3e6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c3e6-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c3e6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c3e6-123">輸入</span><span class="sxs-lookup"><span data-stu-id="6c3e6-123">INPUTS</span></span>

## <span data-ttu-id="6c3e6-124">輸出</span><span class="sxs-lookup"><span data-stu-id="6c3e6-124">OUTPUTS</span></span>

### <span data-ttu-id="6c3e6-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="6c3e6-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="6c3e6-126">筆記</span><span class="sxs-lookup"><span data-stu-id="6c3e6-126">NOTES</span></span>

<span data-ttu-id="6c3e6-127">別名</span><span class="sxs-lookup"><span data-stu-id="6c3e6-127">ALIASES</span></span>

## <span data-ttu-id="6c3e6-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c3e6-128">RELATED LINKS</span></span>

