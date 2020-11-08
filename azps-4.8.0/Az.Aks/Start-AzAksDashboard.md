---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 91e4ec27298fa3fead3041e43f988b96ecf64046
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970739"
---
# <span data-ttu-id="2728f-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="2728f-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="2728f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2728f-102">SYNOPSIS</span></span>
<span data-ttu-id="2728f-103">建立 Kubectl SSH 隧道至 managed 群集的儀表板。</span><span class="sxs-lookup"><span data-stu-id="2728f-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="2728f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2728f-104">SYNTAX</span></span>

### <span data-ttu-id="2728f-105">GroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2728f-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2728f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2728f-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2728f-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2728f-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2728f-108">說明</span><span class="sxs-lookup"><span data-stu-id="2728f-108">DESCRIPTION</span></span>
<span data-ttu-id="2728f-109">建立 Kubectl SSH 隧道至 managed 群集的儀表板。</span><span class="sxs-lookup"><span data-stu-id="2728f-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="2728f-110">SSH 隧道是在稱為 Kubectl-Tunnel 的 PowerShell 作業中設定，可透過執行來找到 `Get-Job` 。</span><span class="sxs-lookup"><span data-stu-id="2728f-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="2728f-111">隧道應該可透過存取 [http://127.0.0.1:8001](http://127.0.0.1:8001) 。</span><span class="sxs-lookup"><span data-stu-id="2728f-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="2728f-112">示例</span><span class="sxs-lookup"><span data-stu-id="2728f-112">EXAMPLES</span></span>

### <span data-ttu-id="2728f-113">啟動 SSH 隧道並開啟瀏覽器至 Kubernetes 儀表板</span><span class="sxs-lookup"><span data-stu-id="2728f-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="2728f-114">參數</span><span class="sxs-lookup"><span data-stu-id="2728f-114">PARAMETERS</span></span>

### <span data-ttu-id="2728f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2728f-115">-DefaultProfile</span></span>
<span data-ttu-id="2728f-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2728f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2728f-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="2728f-117">-DisableBrowser</span></span>
<span data-ttu-id="2728f-118">在建立 kubectl 埠轉寄之後，請不要使用 pop 來開啟瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="2728f-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="2728f-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="2728f-119">-Id</span></span>
<span data-ttu-id="2728f-120">受管理的 Kubernetes 群集的 Id</span><span class="sxs-lookup"><span data-stu-id="2728f-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="2728f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2728f-121">-InputObject</span></span>
<span data-ttu-id="2728f-122">PSKubernetesCluster 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="2728f-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="2728f-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="2728f-123">-ListenPort</span></span>
<span data-ttu-id="2728f-124">儀表板的偵聽埠。</span><span class="sxs-lookup"><span data-stu-id="2728f-124">The listening port for the dashboard.</span></span> <span data-ttu-id="2728f-125">預設值為8003。</span><span class="sxs-lookup"><span data-stu-id="2728f-125">Default value is 8003.</span></span>

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

### <span data-ttu-id="2728f-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="2728f-126">-Name</span></span>
<span data-ttu-id="2728f-127">受管理的 Kubernetes 群集的名稱</span><span class="sxs-lookup"><span data-stu-id="2728f-127">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="2728f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2728f-128">-PassThru</span></span>
<span data-ttu-id="2728f-129">如果傳遞的話，Cmdlet 會傳回 KubeTunnelJob。</span><span class="sxs-lookup"><span data-stu-id="2728f-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="2728f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2728f-130">-ResourceGroupName</span></span>
<span data-ttu-id="2728f-131">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2728f-131">Resource group name</span></span>

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

### <span data-ttu-id="2728f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2728f-132">CommonParameters</span></span>
<span data-ttu-id="2728f-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2728f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2728f-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2728f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2728f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="2728f-135">INPUTS</span></span>

### <span data-ttu-id="2728f-136">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="2728f-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="2728f-137">System.object</span><span class="sxs-lookup"><span data-stu-id="2728f-137">System.String</span></span>

## <span data-ttu-id="2728f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="2728f-138">OUTPUTS</span></span>

### <span data-ttu-id="2728f-139">KubeTunnelJob 中的 Aks</span><span class="sxs-lookup"><span data-stu-id="2728f-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="2728f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="2728f-140">NOTES</span></span>

## <span data-ttu-id="2728f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="2728f-141">RELATED LINKS</span></span>
