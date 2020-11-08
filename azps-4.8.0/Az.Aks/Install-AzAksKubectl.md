---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126639"
---
# <span data-ttu-id="c4118-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="c4118-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="c4118-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4118-102">SYNOPSIS</span></span>
<span data-ttu-id="c4118-103">下載並安裝 kubectl、Kubernetes 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="c4118-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="c4118-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4118-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4118-105">說明</span><span class="sxs-lookup"><span data-stu-id="c4118-105">DESCRIPTION</span></span>
<span data-ttu-id="c4118-106">下載並安裝 kubectl、Kubernetes 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="c4118-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="c4118-107">示例</span><span class="sxs-lookup"><span data-stu-id="c4118-107">EXAMPLES</span></span>

### <span data-ttu-id="c4118-108">下載並安裝最新版本的 kubectl</span><span class="sxs-lookup"><span data-stu-id="c4118-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="c4118-109">參數</span><span class="sxs-lookup"><span data-stu-id="c4118-109">PARAMETERS</span></span>

### <span data-ttu-id="c4118-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4118-110">-AsJob</span></span>
<span data-ttu-id="c4118-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c4118-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4118-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4118-112">-DefaultProfile</span></span>
<span data-ttu-id="c4118-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4118-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4118-114">-目的地</span><span class="sxs-lookup"><span data-stu-id="c4118-114">-Destination</span></span>
<span data-ttu-id="c4118-115">安裝 kubectl 的路徑。</span><span class="sxs-lookup"><span data-stu-id="c4118-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="c4118-116">預設為安裝至 ~/.azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="c4118-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="c4118-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="c4118-117">-DownloadFromMirror</span></span>
<span data-ttu-id="c4118-118">從鏡像網站下載： https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="c4118-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="c4118-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c4118-119">-Force</span></span>
<span data-ttu-id="c4118-120">覆寫現有的 kubectl 而不提示</span><span class="sxs-lookup"><span data-stu-id="c4118-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="c4118-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4118-121">-PassThru</span></span>
<span data-ttu-id="c4118-122">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="c4118-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="c4118-123">-版本</span><span class="sxs-lookup"><span data-stu-id="c4118-123">-Version</span></span>
<span data-ttu-id="c4118-124">要安裝的 kubectl 版本，例如 ' v 1.17.2」。</span><span class="sxs-lookup"><span data-stu-id="c4118-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="c4118-125">預設值：最晚</span><span class="sxs-lookup"><span data-stu-id="c4118-125">Default value: Latest</span></span>

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

### <span data-ttu-id="c4118-126">-確認</span><span class="sxs-lookup"><span data-stu-id="c4118-126">-Confirm</span></span>
<span data-ttu-id="c4118-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c4118-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4118-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4118-128">-WhatIf</span></span>
<span data-ttu-id="c4118-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c4118-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4118-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4118-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4118-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4118-131">CommonParameters</span></span>
<span data-ttu-id="c4118-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4118-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4118-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c4118-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4118-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c4118-134">INPUTS</span></span>

### <span data-ttu-id="c4118-135">所有</span><span class="sxs-lookup"><span data-stu-id="c4118-135">None</span></span>

## <span data-ttu-id="c4118-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c4118-136">OUTPUTS</span></span>

### <span data-ttu-id="c4118-137">System.object</span><span class="sxs-lookup"><span data-stu-id="c4118-137">System.Boolean</span></span>

## <span data-ttu-id="c4118-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c4118-138">NOTES</span></span>

## <span data-ttu-id="c4118-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4118-139">RELATED LINKS</span></span>