---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: 3f38a11cd5d4a124e7db7a99422239f73cbe96dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907973"
---
# <span data-ttu-id="646dc-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="646dc-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="646dc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="646dc-102">SYNOPSIS</span></span>
<span data-ttu-id="646dc-103">Unregister-AzStackHCI Microsoft.AzureStackHCI 雲端資源代表內部部署組，並取消註冊 Azure 內部部署組。</span><span class="sxs-lookup"><span data-stu-id="646dc-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="646dc-104">如果未傳遞任何參數，該組組上可用的登錄資訊會用來取消註冊該組。</span><span class="sxs-lookup"><span data-stu-id="646dc-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="646dc-105">語法</span><span class="sxs-lookup"><span data-stu-id="646dc-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="646dc-106">描述</span><span class="sxs-lookup"><span data-stu-id="646dc-106">DESCRIPTION</span></span>
<span data-ttu-id="646dc-107">Unregister-AzStackHCI Microsoft.AzureStackHCI 雲端資源代表內部部署組，並取消註冊 Azure 內部部署組。</span><span class="sxs-lookup"><span data-stu-id="646dc-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="646dc-108">如果未傳遞任何參數，該組組上可用的登錄資訊會用來取消註冊該組。</span><span class="sxs-lookup"><span data-stu-id="646dc-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="646dc-109">例子</span><span class="sxs-lookup"><span data-stu-id="646dc-109">EXAMPLES</span></span>

### <span data-ttu-id="646dc-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="646dc-110">EXAMPLE 1</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI
Result: Success
```
<span data-ttu-id="646dc-111">其中一個組節點上啟動</span><span class="sxs-lookup"><span data-stu-id="646dc-111">Invoking on one of the cluster node</span></span>

### <span data-ttu-id="646dc-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="646dc-112">EXAMPLE 2</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1
Result: Success
```
<span data-ttu-id="646dc-113">從管理節點中啟動</span><span class="sxs-lookup"><span data-stu-id="646dc-113">Invoking from the management node</span></span>

### <span data-ttu-id="646dc-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="646dc-114">EXAMPLE 3</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False
Result: Success
```
<span data-ttu-id="646dc-115">從 WAC 中引文</span><span class="sxs-lookup"><span data-stu-id="646dc-115">Invoking from WAC</span></span>

### <span data-ttu-id="646dc-116">範例 4</span><span class="sxs-lookup"><span data-stu-id="646dc-116">EXAMPLE 4</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
```
<span data-ttu-id="646dc-117">使用所有參數來引用</span><span class="sxs-lookup"><span data-stu-id="646dc-117">Invoking with all the parameters</span></span>

## <span data-ttu-id="646dc-118">參數</span><span class="sxs-lookup"><span data-stu-id="646dc-118">PARAMETERS</span></span>

### <span data-ttu-id="646dc-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="646dc-119">-AccountId</span></span>
<span data-ttu-id="646dc-120">指定 ARM 存取權杖。</span><span class="sxs-lookup"><span data-stu-id="646dc-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="646dc-121">在 ArmAccessToken 和 GraphAccessToken 中指定此選項可避免 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="646dc-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646dc-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="646dc-122">-ArmAccessToken</span></span>
<span data-ttu-id="646dc-123">指定 ARM 存取權杖。</span><span class="sxs-lookup"><span data-stu-id="646dc-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="646dc-124">與 GraphAccessToken 和 AccountId 一起指定此選項可避免 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="646dc-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646dc-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="646dc-125">-ComputerName</span></span>
<span data-ttu-id="646dc-126">指定要註冊至 Azure 之內部部署組集中的其中一個集區節點。</span><span class="sxs-lookup"><span data-stu-id="646dc-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646dc-127">-認證</span><span class="sxs-lookup"><span data-stu-id="646dc-127">-Credential</span></span>
<span data-ttu-id="646dc-128">指定 ComputerName 的認證。</span><span class="sxs-lookup"><span data-stu-id="646dc-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="646dc-129">預設值為執行 Cmdlet 的目前使用者。</span><span class="sxs-lookup"><span data-stu-id="646dc-129">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646dc-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="646dc-130">-EnvironmentName</span></span>
<span data-ttu-id="646dc-131">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="646dc-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="646dc-132">預設值為 AzureCloud。</span><span class="sxs-lookup"><span data-stu-id="646dc-132">Default is AzureCloud.</span></span>
<span data-ttu-id="646dc-133">有效的值為 AzureCloud、AzureChinaCloud、AzureUSGovernment、AzureGermanCloud、AzurePPE</span><span class="sxs-lookup"><span data-stu-id="646dc-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646dc-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="646dc-134">-GraphAccessToken</span></span>
<span data-ttu-id="646dc-135">指定 Graph 存取權杖。</span><span class="sxs-lookup"><span data-stu-id="646dc-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="646dc-136">在 ArmAccessToken 和 AccountId 中指定此選項可避免 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="646dc-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646dc-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="646dc-137">-ResourceGroupName</span></span>
<span data-ttu-id="646dc-138">指定 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="646dc-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="646dc-139">如果未指定 \<LocalClusterName\> -rg，將會使用做為資源組名。</span><span class="sxs-lookup"><span data-stu-id="646dc-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646dc-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="646dc-140">-ResourceName</span></span>
<span data-ttu-id="646dc-141">指定在 Azure 中建立之資源的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="646dc-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="646dc-142">如果未指定，會使用內部部署組名。</span><span class="sxs-lookup"><span data-stu-id="646dc-142">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646dc-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="646dc-143">-SubscriptionId</span></span>
<span data-ttu-id="646dc-144">指定 Azure 訂閱以建立資源</span><span class="sxs-lookup"><span data-stu-id="646dc-144">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646dc-145">-TenantId</span><span class="sxs-lookup"><span data-stu-id="646dc-145">-TenantId</span></span>
<span data-ttu-id="646dc-146">指定 Azure TenantId。</span><span class="sxs-lookup"><span data-stu-id="646dc-146">Specifies the Azure TenantId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646dc-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="646dc-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="646dc-148">使用裝置代碼驗證，而不使用互動式瀏覽器提示。</span><span class="sxs-lookup"><span data-stu-id="646dc-148">Use device code authentication instead of an interactive browser prompt.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646dc-149">-確認</span><span class="sxs-lookup"><span data-stu-id="646dc-149">-Confirm</span></span>
<span data-ttu-id="646dc-150">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="646dc-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="646dc-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="646dc-151">-WhatIf</span></span>
<span data-ttu-id="646dc-152">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="646dc-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="646dc-153">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="646dc-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="646dc-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646dc-154">CommonParameters</span></span>
<span data-ttu-id="646dc-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="646dc-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646dc-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="646dc-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646dc-157">輸入</span><span class="sxs-lookup"><span data-stu-id="646dc-157">INPUTS</span></span>

## <span data-ttu-id="646dc-158">輸出</span><span class="sxs-lookup"><span data-stu-id="646dc-158">OUTPUTS</span></span>

### <span data-ttu-id="646dc-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="646dc-159">PSCustomObject.</span></span> <span data-ttu-id="646dc-160">在 PSCustomObject 中返回下列屬性</span><span class="sxs-lookup"><span data-stu-id="646dc-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="646dc-161">結果：成功或失敗或取消。</span><span class="sxs-lookup"><span data-stu-id="646dc-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="646dc-162">筆記</span><span class="sxs-lookup"><span data-stu-id="646dc-162">NOTES</span></span>

## <span data-ttu-id="646dc-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="646dc-163">RELATED LINKS</span></span>
