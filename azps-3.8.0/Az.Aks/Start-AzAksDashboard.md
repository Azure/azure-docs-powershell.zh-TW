---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 5a03df969421ea87d907efb5fe23027acfde0834
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957155"
---
# <span data-ttu-id="93d90-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="93d90-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="93d90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93d90-102">SYNOPSIS</span></span>
<span data-ttu-id="93d90-103">建立 Kubectl SSH 隧道至 managed 群集的儀表板。</span><span class="sxs-lookup"><span data-stu-id="93d90-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="93d90-104">句法</span><span class="sxs-lookup"><span data-stu-id="93d90-104">SYNTAX</span></span>

### <span data-ttu-id="93d90-105">GroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="93d90-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93d90-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93d90-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93d90-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93d90-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93d90-108">說明</span><span class="sxs-lookup"><span data-stu-id="93d90-108">DESCRIPTION</span></span>
<span data-ttu-id="93d90-109">建立 Kubectl SSH 隧道至 managed 群集的儀表板。</span><span class="sxs-lookup"><span data-stu-id="93d90-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="93d90-110">SSH 隧道是在稱為 Kubectl-Tunnel 的 PowerShell 作業中設定，可透過執行來找到 `Get-Job` 。</span><span class="sxs-lookup"><span data-stu-id="93d90-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="93d90-111">隧道應該可透過存取 [http://127.0.0.1:8001](http://127.0.0.1:8001) 。</span><span class="sxs-lookup"><span data-stu-id="93d90-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="93d90-112">示例</span><span class="sxs-lookup"><span data-stu-id="93d90-112">EXAMPLES</span></span>

### <span data-ttu-id="93d90-113">啟動 SSH 隧道並開啟瀏覽器至 Kubernetes 儀表板</span><span class="sxs-lookup"><span data-stu-id="93d90-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="93d90-114">參數</span><span class="sxs-lookup"><span data-stu-id="93d90-114">PARAMETERS</span></span>

### <span data-ttu-id="93d90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d90-115">-DefaultProfile</span></span>
<span data-ttu-id="93d90-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93d90-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93d90-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="93d90-117">-DisableBrowser</span></span>
<span data-ttu-id="93d90-118">在建立 kubectl 埠轉寄之後，請不要使用 pop 來開啟瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="93d90-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="93d90-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="93d90-119">-Id</span></span>
<span data-ttu-id="93d90-120">受管理的 Kubernetes 群集的 Id</span><span class="sxs-lookup"><span data-stu-id="93d90-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="93d90-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93d90-121">-InputObject</span></span>
<span data-ttu-id="93d90-122">PSKubernetesCluster 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="93d90-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="93d90-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="93d90-123">-Name</span></span>
<span data-ttu-id="93d90-124">受管理的 Kubernetes 群集的名稱</span><span class="sxs-lookup"><span data-stu-id="93d90-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="93d90-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93d90-125">-PassThru</span></span>
<span data-ttu-id="93d90-126">如果傳遞的話，Cmdlet 會傳回 KubeTunnelJob。</span><span class="sxs-lookup"><span data-stu-id="93d90-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="93d90-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93d90-127">-ResourceGroupName</span></span>
<span data-ttu-id="93d90-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="93d90-128">Resource group name</span></span>

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

### <span data-ttu-id="93d90-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d90-129">CommonParameters</span></span>
<span data-ttu-id="93d90-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93d90-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d90-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="93d90-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d90-132">輸入</span><span class="sxs-lookup"><span data-stu-id="93d90-132">INPUTS</span></span>

### <span data-ttu-id="93d90-133">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="93d90-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="93d90-134">System.object</span><span class="sxs-lookup"><span data-stu-id="93d90-134">System.String</span></span>

## <span data-ttu-id="93d90-135">輸出</span><span class="sxs-lookup"><span data-stu-id="93d90-135">OUTPUTS</span></span>

### <span data-ttu-id="93d90-136">KubeTunnelJob 中的 Aks</span><span class="sxs-lookup"><span data-stu-id="93d90-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="93d90-137">筆記</span><span class="sxs-lookup"><span data-stu-id="93d90-137">NOTES</span></span>

## <span data-ttu-id="93d90-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="93d90-138">RELATED LINKS</span></span>