---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceExtensionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
ms.openlocfilehash: 761d34b4ed2d061b773c136a7d4e2db9f05a9103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136583"
---
# <span data-ttu-id="4e493-101">New-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="4e493-101">New-AzCloudServiceExtensionObject</span></span>

## <span data-ttu-id="4e493-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e493-102">SYNOPSIS</span></span>
<span data-ttu-id="4e493-103">建立延伸的記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="4e493-103">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="4e493-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e493-104">SYNTAX</span></span>

```
New-AzCloudServiceExtensionObject [-AutoUpgradeMinorVersion <Boolean>] [-Name <String>]
 [-ProtectedSetting <String>] [-Publisher <String>] [-RolesAppliedTo <String[]>] [-Setting <String>]
 [-Type <String>] [-TypeHandlerVersion <String>] [<CommonParameters>]
```

## <span data-ttu-id="4e493-105">說明</span><span class="sxs-lookup"><span data-stu-id="4e493-105">DESCRIPTION</span></span>
<span data-ttu-id="4e493-106">建立延伸的記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="4e493-106">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="4e493-107">示例</span><span class="sxs-lookup"><span data-stu-id="4e493-107">EXAMPLES</span></span>

### <span data-ttu-id="4e493-108">範例1：建立 Geneva 延伸物件</span><span class="sxs-lookup"><span data-stu-id="4e493-108">Example 1: Create Geneva extension object</span></span>
```powershell
PS C:\> $extension = New-AzCloudServiceExtensionObject -Name "GenevaExtension" -Publisher "Microsoft.Azure.Geneva" -Type "GenevaMonitoringPaaS" -TypeHandlerVersion "2.14.0.2"
```

<span data-ttu-id="4e493-109">這個命令會建立用來建立或更新雲端服務的 Geneva 延伸物件。</span><span class="sxs-lookup"><span data-stu-id="4e493-109">This command creates Geneva extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="4e493-110">如需詳細資訊，請參閱新 AzCloudService。</span><span class="sxs-lookup"><span data-stu-id="4e493-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="4e493-111">參數</span><span class="sxs-lookup"><span data-stu-id="4e493-111">PARAMETERS</span></span>

### <span data-ttu-id="4e493-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="4e493-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="4e493-113">明確指定 CRP 是否可以在可用時自動將 typeHandlerVersion 升級為較高的次要版本。</span><span class="sxs-lookup"><span data-stu-id="4e493-113">Explicitly specify whether CRP can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>

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

### <span data-ttu-id="4e493-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e493-114">-Name</span></span>
<span data-ttu-id="4e493-115">列名.</span><span class="sxs-lookup"><span data-stu-id="4e493-115">Name.</span></span>

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

### <span data-ttu-id="4e493-116">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="4e493-116">-ProtectedSetting</span></span>
<span data-ttu-id="4e493-117">在傳送至 VM 之前已加密之副檔名的受保護設定。</span><span class="sxs-lookup"><span data-stu-id="4e493-117">Protected settings for the extension which are encrypted before sent to the VM.</span></span>

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

### <span data-ttu-id="4e493-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4e493-118">-Publisher</span></span>
<span data-ttu-id="4e493-119">Publisher.</span><span class="sxs-lookup"><span data-stu-id="4e493-119">Publisher.</span></span>

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

### <span data-ttu-id="4e493-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="4e493-120">-RolesAppliedTo</span></span>
<span data-ttu-id="4e493-121">RolesAppliedTo.</span><span class="sxs-lookup"><span data-stu-id="4e493-121">RolesAppliedTo.</span></span>

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

### <span data-ttu-id="4e493-122">-設定</span><span class="sxs-lookup"><span data-stu-id="4e493-122">-Setting</span></span>
<span data-ttu-id="4e493-123">延伸的公開設定。</span><span class="sxs-lookup"><span data-stu-id="4e493-123">Public settings for the extension.</span></span>

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

### <span data-ttu-id="4e493-124">-類型</span><span class="sxs-lookup"><span data-stu-id="4e493-124">-Type</span></span>
<span data-ttu-id="4e493-125">輸入.</span><span class="sxs-lookup"><span data-stu-id="4e493-125">Type.</span></span>

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

### <span data-ttu-id="4e493-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="4e493-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="4e493-127">TypeHandlerVersion.</span><span class="sxs-lookup"><span data-stu-id="4e493-127">TypeHandlerVersion.</span></span>

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

### <span data-ttu-id="4e493-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e493-128">CommonParameters</span></span>
<span data-ttu-id="4e493-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e493-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e493-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e493-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e493-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4e493-131">INPUTS</span></span>

## <span data-ttu-id="4e493-132">輸出</span><span class="sxs-lookup"><span data-stu-id="4e493-132">OUTPUTS</span></span>

### <span data-ttu-id="4e493-133">Api20201001Preview. CloudService...。</span><span class="sxs-lookup"><span data-stu-id="4e493-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="4e493-134">筆記</span><span class="sxs-lookup"><span data-stu-id="4e493-134">NOTES</span></span>

<span data-ttu-id="4e493-135">別名</span><span class="sxs-lookup"><span data-stu-id="4e493-135">ALIASES</span></span>

## <span data-ttu-id="4e493-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e493-136">RELATED LINKS</span></span>

