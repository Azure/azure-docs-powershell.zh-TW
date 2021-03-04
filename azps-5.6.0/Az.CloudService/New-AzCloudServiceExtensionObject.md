---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceExtensionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
ms.openlocfilehash: d37a717ba87771310de4f1944e3865712e00554e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910534"
---
# <span data-ttu-id="e3d41-101">New-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="e3d41-101">New-AzCloudServiceExtensionObject</span></span>

## <span data-ttu-id="e3d41-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e3d41-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d41-103">建立記憶體內物件以用於擴充功能</span><span class="sxs-lookup"><span data-stu-id="e3d41-103">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="e3d41-104">語法</span><span class="sxs-lookup"><span data-stu-id="e3d41-104">SYNTAX</span></span>

```
New-AzCloudServiceExtensionObject [-AutoUpgradeMinorVersion <Boolean>] [-Name <String>]
 [-ProtectedSetting <String>] [-Publisher <String>] [-RolesAppliedTo <String[]>] [-Setting <String>]
 [-Type <String>] [-TypeHandlerVersion <String>] [<CommonParameters>]
```

## <span data-ttu-id="e3d41-105">描述</span><span class="sxs-lookup"><span data-stu-id="e3d41-105">DESCRIPTION</span></span>
<span data-ttu-id="e3d41-106">建立記憶體內物件以用於擴充功能</span><span class="sxs-lookup"><span data-stu-id="e3d41-106">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="e3d41-107">例子</span><span class="sxs-lookup"><span data-stu-id="e3d41-107">EXAMPLES</span></span>

### <span data-ttu-id="e3d41-108">範例 1：建立擴充物件</span><span class="sxs-lookup"><span data-stu-id="e3d41-108">Example 1: Create Geneva extension object</span></span>
```powershell
PS C:\> $extension = New-AzCloudServiceExtensionObject -Name "GenevaExtension" -Publisher "Microsoft.Azure.Geneva" -Type "GenevaMonitoringPaaS" -TypeHandlerVersion "2.14.0.2"
```

<span data-ttu-id="e3d41-109">此命令會建立一個擴充物件，用於建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="e3d41-109">This command creates Geneva extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="e3d41-110">詳情請參閱 New-AzCloudService。</span><span class="sxs-lookup"><span data-stu-id="e3d41-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="e3d41-111">參數</span><span class="sxs-lookup"><span data-stu-id="e3d41-111">PARAMETERS</span></span>

### <span data-ttu-id="e3d41-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e3d41-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e3d41-113">明確指定 CRP 是否可以自動將 TypeHandlerVersion 升級至較次要版本，當這些次要版本可供使用時。</span><span class="sxs-lookup"><span data-stu-id="e3d41-113">Explicitly specify whether CRP can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d41-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3d41-114">-Name</span></span>
<span data-ttu-id="e3d41-115">名字。</span><span class="sxs-lookup"><span data-stu-id="e3d41-115">Name.</span></span>

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

### <span data-ttu-id="e3d41-116">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="e3d41-116">-ProtectedSetting</span></span>
<span data-ttu-id="e3d41-117">在傳輸至 VM 之前經過加密的擴充功能之受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="e3d41-117">Protected settings for the extension which are encrypted before sent to the VM.</span></span>

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

### <span data-ttu-id="e3d41-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e3d41-118">-Publisher</span></span>
<span data-ttu-id="e3d41-119">出版商。</span><span class="sxs-lookup"><span data-stu-id="e3d41-119">Publisher.</span></span>

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

### <span data-ttu-id="e3d41-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="e3d41-120">-RolesAppliedTo</span></span>
<span data-ttu-id="e3d41-121">RolesAppliedTo.</span><span class="sxs-lookup"><span data-stu-id="e3d41-121">RolesAppliedTo.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d41-122">-設定</span><span class="sxs-lookup"><span data-stu-id="e3d41-122">-Setting</span></span>
<span data-ttu-id="e3d41-123">擴充功能公用設定。</span><span class="sxs-lookup"><span data-stu-id="e3d41-123">Public settings for the extension.</span></span>

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

### <span data-ttu-id="e3d41-124">-類型</span><span class="sxs-lookup"><span data-stu-id="e3d41-124">-Type</span></span>
<span data-ttu-id="e3d41-125">類型。</span><span class="sxs-lookup"><span data-stu-id="e3d41-125">Type.</span></span>

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

### <span data-ttu-id="e3d41-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e3d41-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="e3d41-127">TypeHandlerVersion。</span><span class="sxs-lookup"><span data-stu-id="e3d41-127">TypeHandlerVersion.</span></span>

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

### <span data-ttu-id="e3d41-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d41-128">CommonParameters</span></span>
<span data-ttu-id="e3d41-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e3d41-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d41-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3d41-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d41-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e3d41-131">INPUTS</span></span>

## <span data-ttu-id="e3d41-132">輸出</span><span class="sxs-lookup"><span data-stu-id="e3d41-132">OUTPUTS</span></span>

### <span data-ttu-id="e3d41-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.extension</span><span class="sxs-lookup"><span data-stu-id="e3d41-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="e3d41-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e3d41-134">NOTES</span></span>

<span data-ttu-id="e3d41-135">別名</span><span class="sxs-lookup"><span data-stu-id="e3d41-135">ALIASES</span></span>

## <span data-ttu-id="e3d41-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3d41-136">RELATED LINKS</span></span>

