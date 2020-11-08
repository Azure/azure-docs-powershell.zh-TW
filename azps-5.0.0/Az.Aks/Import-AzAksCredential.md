---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: fe4e56e809dd2cda7c650e24b55ae3867a23a7b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138560"
---
# <span data-ttu-id="4e134-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="4e134-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="4e134-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e134-102">SYNOPSIS</span></span>
<span data-ttu-id="4e134-103">匯入及合併 managed Kubernetes 群集的 Kubectl config。</span><span class="sxs-lookup"><span data-stu-id="4e134-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="4e134-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e134-104">SYNTAX</span></span>

### <span data-ttu-id="4e134-105">GroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4e134-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e134-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e134-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e134-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e134-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e134-108">說明</span><span class="sxs-lookup"><span data-stu-id="4e134-108">DESCRIPTION</span></span>
<span data-ttu-id="4e134-109">匯入及合併 managed Kubernetes 群集的 Kubectl config。</span><span class="sxs-lookup"><span data-stu-id="4e134-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="4e134-110">示例</span><span class="sxs-lookup"><span data-stu-id="4e134-110">EXAMPLES</span></span>

### <span data-ttu-id="4e134-111">匯入及合併 Kubectl config</span><span class="sxs-lookup"><span data-stu-id="4e134-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="4e134-112">參數</span><span class="sxs-lookup"><span data-stu-id="4e134-112">PARAMETERS</span></span>

### <span data-ttu-id="4e134-113">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="4e134-113">-Admin</span></span>
<span data-ttu-id="4e134-114">取得 [clusterAdmin' kubectl config]，而不是預設的「clusterUser」。</span><span class="sxs-lookup"><span data-stu-id="4e134-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="4e134-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="4e134-115">-ConfigPath</span></span>
<span data-ttu-id="4e134-116">要建立或更新的 kubectl config 檔案。</span><span class="sxs-lookup"><span data-stu-id="4e134-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="4e134-117">使用 "-" 改為列印 YAML 至 stdout。</span><span class="sxs-lookup"><span data-stu-id="4e134-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="4e134-118">預設值：% Home%/.kube/config。</span><span class="sxs-lookup"><span data-stu-id="4e134-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="4e134-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e134-119">-DefaultProfile</span></span>
<span data-ttu-id="4e134-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e134-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e134-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4e134-121">-Force</span></span>
<span data-ttu-id="4e134-122">匯入 Kubernetes config （即使是預設值）</span><span class="sxs-lookup"><span data-stu-id="4e134-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="4e134-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="4e134-123">-Id</span></span>
<span data-ttu-id="4e134-124">受管理的 Kubernetes 群集的 Id</span><span class="sxs-lookup"><span data-stu-id="4e134-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="4e134-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e134-125">-InputObject</span></span>
<span data-ttu-id="4e134-126">PSKubernetesCluster 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="4e134-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="4e134-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e134-127">-Name</span></span>
<span data-ttu-id="4e134-128">受管理的 Kubernetes 群集的名稱</span><span class="sxs-lookup"><span data-stu-id="4e134-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="4e134-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e134-129">-PassThru</span></span>
<span data-ttu-id="4e134-130">如果匯入成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="4e134-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="4e134-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e134-131">-ResourceGroupName</span></span>
<span data-ttu-id="4e134-132">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="4e134-132">Resource group name</span></span>

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

### <span data-ttu-id="4e134-133">-確認</span><span class="sxs-lookup"><span data-stu-id="4e134-133">-Confirm</span></span>
<span data-ttu-id="4e134-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4e134-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e134-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e134-135">-WhatIf</span></span>
<span data-ttu-id="4e134-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e134-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e134-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e134-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e134-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e134-138">CommonParameters</span></span>
<span data-ttu-id="4e134-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e134-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e134-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e134-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e134-141">輸入</span><span class="sxs-lookup"><span data-stu-id="4e134-141">INPUTS</span></span>

### <span data-ttu-id="4e134-142">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="4e134-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="4e134-143">System.object</span><span class="sxs-lookup"><span data-stu-id="4e134-143">System.String</span></span>

## <span data-ttu-id="4e134-144">輸出</span><span class="sxs-lookup"><span data-stu-id="4e134-144">OUTPUTS</span></span>

### <span data-ttu-id="4e134-145">System.object</span><span class="sxs-lookup"><span data-stu-id="4e134-145">System.String</span></span>

## <span data-ttu-id="4e134-146">筆記</span><span class="sxs-lookup"><span data-stu-id="4e134-146">NOTES</span></span>

## <span data-ttu-id="4e134-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e134-147">RELATED LINKS</span></span>
