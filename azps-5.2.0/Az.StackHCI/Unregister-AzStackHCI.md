---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e063af1a489c9e68845f087e339f42de65281501
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280178"
---
# <span data-ttu-id="f4d71-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="f4d71-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="f4d71-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4d71-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d71-103">Unregister-AzStackHCI 刪除代表內部部署群集的 AzureStackHCI 雲端資源，並以 Azure 登出內部部署群集。</span><span class="sxs-lookup"><span data-stu-id="f4d71-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="f4d71-104">如果未傳遞任何參數，則會使用在群集上註冊的資訊來登出群集。</span><span class="sxs-lookup"><span data-stu-id="f4d71-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="f4d71-105">句法</span><span class="sxs-lookup"><span data-stu-id="f4d71-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4d71-106">說明</span><span class="sxs-lookup"><span data-stu-id="f4d71-106">DESCRIPTION</span></span>
<span data-ttu-id="f4d71-107">Unregister-AzStackHCI 刪除代表內部部署群集的 AzureStackHCI 雲端資源，並以 Azure 登出內部部署群集。</span><span class="sxs-lookup"><span data-stu-id="f4d71-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="f4d71-108">如果未傳遞任何參數，則會使用在群集上註冊的資訊來登出群集。</span><span class="sxs-lookup"><span data-stu-id="f4d71-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="f4d71-109">示例</span><span class="sxs-lookup"><span data-stu-id="f4d71-109">EXAMPLES</span></span>

### <span data-ttu-id="f4d71-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f4d71-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="f4d71-111">C:\PS \> 取消註冊-AzStackHCI 結果：成功</span><span class="sxs-lookup"><span data-stu-id="f4d71-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="f4d71-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f4d71-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="f4d71-113">C:\PS \> 取消註冊-AzStackHCI-ComputerName ClusterNode1 結果：成功</span><span class="sxs-lookup"><span data-stu-id="f4d71-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="f4d71-114">範例3</span><span class="sxs-lookup"><span data-stu-id="f4d71-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="f4d71-115">C:\PS \> [取消註冊-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd]-ArmAccessToken etyer .。。ere =-GraphAccessToken acyee。rerrer- user1@corp1.com DemoHCICluster3-ResourceGroupName DemoHCIRG-確認： $False 結果：成功</span><span class="sxs-lookup"><span data-stu-id="f4d71-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="f4d71-116">範例4</span><span class="sxs-lookup"><span data-stu-id="f4d71-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="f4d71-117">C:\PS \> 取消註冊-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-CoNtext.resourcename HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer .。。ere =-GraphAccessToken acee。rerrer- user1@corp1.com EnvironmentName AzureCloud-ComputerName node1hci-認證 Get-Credential 結果：成功</span><span class="sxs-lookup"><span data-stu-id="f4d71-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="f4d71-118">參數</span><span class="sxs-lookup"><span data-stu-id="f4d71-118">PARAMETERS</span></span>

### <span data-ttu-id="f4d71-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="f4d71-119">-AccountId</span></span>
<span data-ttu-id="f4d71-120">指定 ARM 存取權杖。</span><span class="sxs-lookup"><span data-stu-id="f4d71-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="f4d71-121">將它與 ArmAccessToken 和 GraphAccessToken 一起指定，將會避開 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="f4d71-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="f4d71-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="f4d71-122">-ArmAccessToken</span></span>
<span data-ttu-id="f4d71-123">指定 ARM 存取權杖。</span><span class="sxs-lookup"><span data-stu-id="f4d71-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="f4d71-124">將此指定與 GraphAccessToken 和 AccountId 搭配使用，就可以避免 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="f4d71-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="f4d71-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="f4d71-125">-ComputerName</span></span>
<span data-ttu-id="f4d71-126">指定登錄至 Azure 之內部部署群集中的其中一個叢集節點。</span><span class="sxs-lookup"><span data-stu-id="f4d71-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="f4d71-127">-認證</span><span class="sxs-lookup"><span data-stu-id="f4d71-127">-Credential</span></span>
<span data-ttu-id="f4d71-128">指定 ComputerName 的認證。</span><span class="sxs-lookup"><span data-stu-id="f4d71-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="f4d71-129">[預設值] 是執行 Cmdlet 的目前使用者。</span><span class="sxs-lookup"><span data-stu-id="f4d71-129">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="f4d71-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="f4d71-130">-EnvironmentName</span></span>
<span data-ttu-id="f4d71-131">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="f4d71-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="f4d71-132">預設值為 AzureCloud。</span><span class="sxs-lookup"><span data-stu-id="f4d71-132">Default is AzureCloud.</span></span>
<span data-ttu-id="f4d71-133">有效值為 AzureCloud、AzureChinaCloud、AzureUSGovernment、AzureGermanCloud、AzurePPE</span><span class="sxs-lookup"><span data-stu-id="f4d71-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="f4d71-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="f4d71-134">-GraphAccessToken</span></span>
<span data-ttu-id="f4d71-135">指定圖形存取權杖。</span><span class="sxs-lookup"><span data-stu-id="f4d71-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="f4d71-136">將此指定與 ArmAccessToken 和 AccountId 搭配使用，就可以避免 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="f4d71-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="f4d71-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d71-137">-ResourceGroupName</span></span>
<span data-ttu-id="f4d71-138">指定 Azure 資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f4d71-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="f4d71-139">如果沒有指定 \<LocalClusterName\> ，則會將 rg 用作資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f4d71-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="f4d71-140">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="f4d71-140">-ResourceName</span></span>
<span data-ttu-id="f4d71-141">指定在 Azure 中建立之資源的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f4d71-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="f4d71-142">如果沒有指定，則會使用內部部署的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="f4d71-142">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="f4d71-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4d71-143">-SubscriptionId</span></span>
<span data-ttu-id="f4d71-144">指定 Azure 訂閱以建立資源</span><span class="sxs-lookup"><span data-stu-id="f4d71-144">Specifies the Azure Subscription to create the resource</span></span>

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

### <span data-ttu-id="f4d71-145">-TenantId</span><span class="sxs-lookup"><span data-stu-id="f4d71-145">-TenantId</span></span>
<span data-ttu-id="f4d71-146">指定 Azure TenantId。</span><span class="sxs-lookup"><span data-stu-id="f4d71-146">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="f4d71-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="f4d71-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="f4d71-148">使用裝置程式碼驗證，而非互動式瀏覽器提示。</span><span class="sxs-lookup"><span data-stu-id="f4d71-148">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="f4d71-149">-確認</span><span class="sxs-lookup"><span data-stu-id="f4d71-149">-Confirm</span></span>
<span data-ttu-id="f4d71-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4d71-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4d71-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4d71-151">-WhatIf</span></span>
<span data-ttu-id="f4d71-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4d71-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4d71-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4d71-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4d71-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d71-154">CommonParameters</span></span>
<span data-ttu-id="f4d71-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4d71-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d71-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f4d71-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d71-157">輸入</span><span class="sxs-lookup"><span data-stu-id="f4d71-157">INPUTS</span></span>

## <span data-ttu-id="f4d71-158">輸出</span><span class="sxs-lookup"><span data-stu-id="f4d71-158">OUTPUTS</span></span>

### <span data-ttu-id="f4d71-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="f4d71-159">PSCustomObject.</span></span> <span data-ttu-id="f4d71-160">在 PSCustomObject 中傳回下列屬性</span><span class="sxs-lookup"><span data-stu-id="f4d71-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="f4d71-161">結果：成功或失敗或已取消。</span><span class="sxs-lookup"><span data-stu-id="f4d71-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="f4d71-162">筆記</span><span class="sxs-lookup"><span data-stu-id="f4d71-162">NOTES</span></span>

## <span data-ttu-id="f4d71-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4d71-163">RELATED LINKS</span></span>
