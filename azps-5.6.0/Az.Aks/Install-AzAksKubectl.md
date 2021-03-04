---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 6a3dc975c34d4938235ce95743f73f833a948b49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905634"
---
# <span data-ttu-id="e9417-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="e9417-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="e9417-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e9417-102">SYNOPSIS</span></span>
<span data-ttu-id="e9417-103">下載並安裝 kubectl，即 Kubernetes 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="e9417-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="e9417-104">語法</span><span class="sxs-lookup"><span data-stu-id="e9417-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9417-105">描述</span><span class="sxs-lookup"><span data-stu-id="e9417-105">DESCRIPTION</span></span>
<span data-ttu-id="e9417-106">下載並安裝 kubectl，即 Kubernetes 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="e9417-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="e9417-107">例子</span><span class="sxs-lookup"><span data-stu-id="e9417-107">EXAMPLES</span></span>

### <span data-ttu-id="e9417-108">下載並安裝最新版本的 kubectl</span><span class="sxs-lookup"><span data-stu-id="e9417-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="e9417-109">參數</span><span class="sxs-lookup"><span data-stu-id="e9417-109">PARAMETERS</span></span>

### <span data-ttu-id="e9417-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9417-110">-AsJob</span></span>
<span data-ttu-id="e9417-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e9417-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9417-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9417-112">-DefaultProfile</span></span>
<span data-ttu-id="e9417-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9417-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9417-114">-目的地</span><span class="sxs-lookup"><span data-stu-id="e9417-114">-Destination</span></span>
<span data-ttu-id="e9417-115">安裝 kubectl 的路徑。</span><span class="sxs-lookup"><span data-stu-id="e9417-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="e9417-116">預設安裝至 ~/.azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="e9417-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="e9417-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="e9417-117">-DownloadFromMirror</span></span>
<span data-ttu-id="e9417-118">從鏡像網站下載： https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="e9417-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9417-119">-強制</span><span class="sxs-lookup"><span data-stu-id="e9417-119">-Force</span></span>
<span data-ttu-id="e9417-120">覆寫現有的kubectl而不提示</span><span class="sxs-lookup"><span data-stu-id="e9417-120">Overwrite existing kubectl without prompt</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9417-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9417-121">-PassThru</span></span>
<span data-ttu-id="e9417-122">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="e9417-122">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9417-123">-版本</span><span class="sxs-lookup"><span data-stu-id="e9417-123">-Version</span></span>
<span data-ttu-id="e9417-124">要安裝的 kubectl 版本，例如'v1.17.2'。</span><span class="sxs-lookup"><span data-stu-id="e9417-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="e9417-125">預設值：最新</span><span class="sxs-lookup"><span data-stu-id="e9417-125">Default value: Latest</span></span>

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

### <span data-ttu-id="e9417-126">-確認</span><span class="sxs-lookup"><span data-stu-id="e9417-126">-Confirm</span></span>
<span data-ttu-id="e9417-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e9417-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9417-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9417-128">-WhatIf</span></span>
<span data-ttu-id="e9417-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9417-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9417-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9417-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9417-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9417-131">CommonParameters</span></span>
<span data-ttu-id="e9417-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e9417-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9417-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9417-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9417-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e9417-134">INPUTS</span></span>

### <span data-ttu-id="e9417-135">沒有</span><span class="sxs-lookup"><span data-stu-id="e9417-135">None</span></span>

## <span data-ttu-id="e9417-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e9417-136">OUTPUTS</span></span>

### <span data-ttu-id="e9417-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e9417-137">System.Boolean</span></span>

## <span data-ttu-id="e9417-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e9417-138">NOTES</span></span>

## <span data-ttu-id="e9417-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9417-139">RELATED LINKS</span></span>
