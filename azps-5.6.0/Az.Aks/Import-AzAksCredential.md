---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: 06ea31f48dbe3b1d5a103598f7f16953bfc449ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905641"
---
# <span data-ttu-id="6eadd-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="6eadd-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="6eadd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6eadd-102">SYNOPSIS</span></span>
<span data-ttu-id="6eadd-103">匯入及合併受管理的 Kubernetes Cluster 的 Kubectl 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6eadd-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="6eadd-104">語法</span><span class="sxs-lookup"><span data-stu-id="6eadd-104">SYNTAX</span></span>

### <span data-ttu-id="6eadd-105">GroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6eadd-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eadd-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eadd-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eadd-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eadd-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eadd-108">描述</span><span class="sxs-lookup"><span data-stu-id="6eadd-108">DESCRIPTION</span></span>
<span data-ttu-id="6eadd-109">匯入及合併受管理的 Kubernetes Cluster 的 Kubectl 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6eadd-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="6eadd-110">例子</span><span class="sxs-lookup"><span data-stu-id="6eadd-110">EXAMPLES</span></span>

### <span data-ttu-id="6eadd-111">匯入及合併 Kubectl config</span><span class="sxs-lookup"><span data-stu-id="6eadd-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="6eadd-112">參數</span><span class="sxs-lookup"><span data-stu-id="6eadd-112">PARAMETERS</span></span>

### <span data-ttu-id="6eadd-113">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="6eadd-113">-Admin</span></span>
<span data-ttu-id="6eadd-114">取得 'clusterAdmin' kubectl config，而不是預設的 'clusterUser'。</span><span class="sxs-lookup"><span data-stu-id="6eadd-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="6eadd-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="6eadd-115">-ConfigPath</span></span>
<span data-ttu-id="6eadd-116">要建立或更新的保存設定檔。</span><span class="sxs-lookup"><span data-stu-id="6eadd-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="6eadd-117">請改為使用 '-' 列印 YAML 來列印。</span><span class="sxs-lookup"><span data-stu-id="6eadd-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="6eadd-118">預設值：%Home%/.kube/config。</span><span class="sxs-lookup"><span data-stu-id="6eadd-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="6eadd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eadd-119">-DefaultProfile</span></span>
<span data-ttu-id="6eadd-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6eadd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eadd-121">-強制</span><span class="sxs-lookup"><span data-stu-id="6eadd-121">-Force</span></span>
<span data-ttu-id="6eadd-122">即使這是預設值，也一併輸入 Kubernetes config</span><span class="sxs-lookup"><span data-stu-id="6eadd-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="6eadd-123">-Id</span><span class="sxs-lookup"><span data-stu-id="6eadd-123">-Id</span></span>
<span data-ttu-id="6eadd-124">受管理的Kubernetes 集的識別碼</span><span class="sxs-lookup"><span data-stu-id="6eadd-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6eadd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6eadd-125">-InputObject</span></span>
<span data-ttu-id="6eadd-126">PSKubernetesCluster 物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="6eadd-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6eadd-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="6eadd-127">-Name</span></span>
<span data-ttu-id="6eadd-128">受管理的Kubernetes 組名</span><span class="sxs-lookup"><span data-stu-id="6eadd-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6eadd-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6eadd-129">-PassThru</span></span>
<span data-ttu-id="6eadd-130">如果成功進行導入，則返回 True</span><span class="sxs-lookup"><span data-stu-id="6eadd-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="6eadd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eadd-131">-ResourceGroupName</span></span>
<span data-ttu-id="6eadd-132">資源組名</span><span class="sxs-lookup"><span data-stu-id="6eadd-132">Resource group name</span></span>

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

### <span data-ttu-id="6eadd-133">-確認</span><span class="sxs-lookup"><span data-stu-id="6eadd-133">-Confirm</span></span>
<span data-ttu-id="6eadd-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6eadd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eadd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eadd-135">-WhatIf</span></span>
<span data-ttu-id="6eadd-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6eadd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eadd-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eadd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eadd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eadd-138">CommonParameters</span></span>
<span data-ttu-id="6eadd-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6eadd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eadd-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6eadd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eadd-141">輸入</span><span class="sxs-lookup"><span data-stu-id="6eadd-141">INPUTS</span></span>

### <span data-ttu-id="6eadd-142">Microsoft.Azure.Commands.Aks.models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="6eadd-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="6eadd-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6eadd-143">System.String</span></span>

## <span data-ttu-id="6eadd-144">輸出</span><span class="sxs-lookup"><span data-stu-id="6eadd-144">OUTPUTS</span></span>

### <span data-ttu-id="6eadd-145">System.String</span><span class="sxs-lookup"><span data-stu-id="6eadd-145">System.String</span></span>

## <span data-ttu-id="6eadd-146">筆記</span><span class="sxs-lookup"><span data-stu-id="6eadd-146">NOTES</span></span>

## <span data-ttu-id="6eadd-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="6eadd-147">RELATED LINKS</span></span>
