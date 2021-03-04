---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 5202f4c86d1d83d6e337c61ee6fc0f72a2b031de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913989"
---
# <span data-ttu-id="e31e2-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="e31e2-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="e31e2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e31e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e31e2-103">在受管理之組儀表板上建立 Kubectl SSH 星型。</span><span class="sxs-lookup"><span data-stu-id="e31e2-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="e31e2-104">語法</span><span class="sxs-lookup"><span data-stu-id="e31e2-104">SYNTAX</span></span>

### <span data-ttu-id="e31e2-105">GroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e31e2-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e31e2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e31e2-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e31e2-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e31e2-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e31e2-108">描述</span><span class="sxs-lookup"><span data-stu-id="e31e2-108">DESCRIPTION</span></span>
<span data-ttu-id="e31e2-109">在受管理之組儀表板上建立 Kubectl SSH 星型。</span><span class="sxs-lookup"><span data-stu-id="e31e2-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="e31e2-110">SSH 的外包裝是在名為 Kubectl-Tunnel 的 PowerShell 工作中設定，而且可以執行來找到 `Get-Job` 。</span><span class="sxs-lookup"><span data-stu-id="e31e2-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="e31e2-111">應該可以透過 . [http://127.0.0.1:8001](http://127.0.0.1:8001)</span><span class="sxs-lookup"><span data-stu-id="e31e2-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="e31e2-112">例子</span><span class="sxs-lookup"><span data-stu-id="e31e2-112">EXAMPLES</span></span>

### <span data-ttu-id="e31e2-113">啟動 SSH 儀表板，並開啟瀏覽器至 Kubernetes 儀表板</span><span class="sxs-lookup"><span data-stu-id="e31e2-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="e31e2-114">參數</span><span class="sxs-lookup"><span data-stu-id="e31e2-114">PARAMETERS</span></span>

### <span data-ttu-id="e31e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e31e2-115">-DefaultProfile</span></span>
<span data-ttu-id="e31e2-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e31e2-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="e31e2-117">-DisableBrowser</span></span>
<span data-ttu-id="e31e2-118">建立kubectl 埠轉轉之後，請勿彈出開啟瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="e31e2-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="e31e2-119">-Id</span><span class="sxs-lookup"><span data-stu-id="e31e2-119">-Id</span></span>
<span data-ttu-id="e31e2-120">受管理的Kubernetes 集的識別碼</span><span class="sxs-lookup"><span data-stu-id="e31e2-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31e2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e31e2-121">-InputObject</span></span>
<span data-ttu-id="e31e2-122">PSKubernetesCluster 物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="e31e2-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e31e2-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="e31e2-123">-ListenPort</span></span>
<span data-ttu-id="e31e2-124">儀表板的聆聽埠。</span><span class="sxs-lookup"><span data-stu-id="e31e2-124">The listening port for the dashboard.</span></span> <span data-ttu-id="e31e2-125">預設值為 8003。</span><span class="sxs-lookup"><span data-stu-id="e31e2-125">Default value is 8003.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e31e2-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="e31e2-126">-Name</span></span>
<span data-ttu-id="e31e2-127">受管理的Kubernetes 組名</span><span class="sxs-lookup"><span data-stu-id="e31e2-127">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e31e2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e31e2-128">-PassThru</span></span>
<span data-ttu-id="e31e2-129">如果傳遞，Cmdlet 會傳回 KubeTun有Job。</span><span class="sxs-lookup"><span data-stu-id="e31e2-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="e31e2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e31e2-130">-ResourceGroupName</span></span>
<span data-ttu-id="e31e2-131">資源組名</span><span class="sxs-lookup"><span data-stu-id="e31e2-131">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e31e2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e31e2-132">CommonParameters</span></span>
<span data-ttu-id="e31e2-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e31e2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e31e2-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e31e2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e31e2-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e31e2-135">INPUTS</span></span>

### <span data-ttu-id="e31e2-136">Microsoft.Azure.Commands.Aks.models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="e31e2-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="e31e2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e31e2-137">System.String</span></span>

## <span data-ttu-id="e31e2-138">輸出</span><span class="sxs-lookup"><span data-stu-id="e31e2-138">OUTPUTS</span></span>

### <span data-ttu-id="e31e2-139">Microsoft.Azure.Commands.Aks.KubeTunureJob</span><span class="sxs-lookup"><span data-stu-id="e31e2-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="e31e2-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e31e2-140">NOTES</span></span>

## <span data-ttu-id="e31e2-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="e31e2-141">RELATED LINKS</span></span>
