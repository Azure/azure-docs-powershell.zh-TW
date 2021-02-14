---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceRoleProfilePropertiesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
ms.openlocfilehash: c9e41a6a4fa7a89db31304dc343da466e8632a74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129910"
---
# <span data-ttu-id="2b482-101">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="2b482-101">New-AzCloudServiceRoleProfilePropertiesObject</span></span>

## <span data-ttu-id="2b482-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b482-102">SYNOPSIS</span></span>
<span data-ttu-id="2b482-103">為 CloudServiceRoleProfileProperties 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="2b482-103">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="2b482-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b482-104">SYNTAX</span></span>

```
New-AzCloudServiceRoleProfilePropertiesObject [-Name <String>] [-SkuCapacity <Int64>] [-SkuName <String>]
 [-SkuTier <String>] [<CommonParameters>]
```

## <span data-ttu-id="2b482-105">說明</span><span class="sxs-lookup"><span data-stu-id="2b482-105">DESCRIPTION</span></span>
<span data-ttu-id="2b482-106">為 CloudServiceRoleProfileProperties 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="2b482-106">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="2b482-107">示例</span><span class="sxs-lookup"><span data-stu-id="2b482-107">EXAMPLES</span></span>

### <span data-ttu-id="2b482-108">範例1：建立角色配置檔案屬性物件</span><span class="sxs-lookup"><span data-stu-id="2b482-108">Example 1: Create role profile properties object</span></span>
```powershell
$role = New-AzCloudServiceRoleProfilePropertiesObject -Name 'WebRole' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
```

<span data-ttu-id="2b482-109">這個命令會建立角色配置檔案屬性物件，以用於建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="2b482-109">This command creates role profile properties object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="2b482-110">如需詳細資訊，請參閱新 AzCloudService。</span><span class="sxs-lookup"><span data-stu-id="2b482-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="2b482-111">參數</span><span class="sxs-lookup"><span data-stu-id="2b482-111">PARAMETERS</span></span>

### <span data-ttu-id="2b482-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b482-112">-Name</span></span>
<span data-ttu-id="2b482-113">角色設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b482-113">Name of role profile.</span></span>

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

### <span data-ttu-id="2b482-114">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2b482-114">-SkuCapacity</span></span>
<span data-ttu-id="2b482-115">指定雲端服務中的角色實例數。</span><span class="sxs-lookup"><span data-stu-id="2b482-115">Specifies the number of role instances in the cloud service.</span></span>

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

### <span data-ttu-id="2b482-116">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2b482-116">-SkuName</span></span>
<span data-ttu-id="2b482-117">Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="2b482-117">The sku name.</span></span>

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

### <span data-ttu-id="2b482-118">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2b482-118">-SkuTier</span></span>
<span data-ttu-id="2b482-119">SkuTier.</span><span class="sxs-lookup"><span data-stu-id="2b482-119">SkuTier.</span></span>

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

### <span data-ttu-id="2b482-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b482-120">CommonParameters</span></span>
<span data-ttu-id="2b482-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b482-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b482-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2b482-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b482-123">輸入</span><span class="sxs-lookup"><span data-stu-id="2b482-123">INPUTS</span></span>

## <span data-ttu-id="2b482-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2b482-124">OUTPUTS</span></span>

### <span data-ttu-id="2b482-125">CloudServiceRoleProfileProperties （CloudService）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="2b482-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="2b482-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2b482-126">NOTES</span></span>

<span data-ttu-id="2b482-127">別名</span><span class="sxs-lookup"><span data-stu-id="2b482-127">ALIASES</span></span>

## <span data-ttu-id="2b482-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b482-128">RELATED LINKS</span></span>

