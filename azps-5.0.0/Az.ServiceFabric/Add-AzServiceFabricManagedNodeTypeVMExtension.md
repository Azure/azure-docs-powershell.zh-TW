---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141245"
---
# <span data-ttu-id="d966c-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="d966c-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="d966c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d966c-102">SYNOPSIS</span></span>
<span data-ttu-id="d966c-103">新增 vm 延伸至節點類型。</span><span class="sxs-lookup"><span data-stu-id="d966c-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="d966c-104">句法</span><span class="sxs-lookup"><span data-stu-id="d966c-104">SYNTAX</span></span>

### <span data-ttu-id="d966c-105">ByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="d966c-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d966c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d966c-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d966c-107">說明</span><span class="sxs-lookup"><span data-stu-id="d966c-107">DESCRIPTION</span></span>
<span data-ttu-id="d966c-108">新增 vm 延伸至節點類型。</span><span class="sxs-lookup"><span data-stu-id="d966c-108">Add vm extension to the node type.</span></span> <span data-ttu-id="d966c-109">這會將延伸新增至 underliying 的「虛擬電腦規模集資源」。</span><span class="sxs-lookup"><span data-stu-id="d966c-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="d966c-110">示例</span><span class="sxs-lookup"><span data-stu-id="d966c-110">EXAMPLES</span></span>

### <span data-ttu-id="d966c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d966c-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="d966c-112">這個命令會將延伸新增至節點類型。</span><span class="sxs-lookup"><span data-stu-id="d966c-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="d966c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="d966c-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="d966c-114">這個命令會將副檔名與 [設定] 和 [受保護的設定] 新增至節點類型。</span><span class="sxs-lookup"><span data-stu-id="d966c-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="d966c-115">範例3</span><span class="sxs-lookup"><span data-stu-id="d966c-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="d966c-116">這個命令會使用管道將延伸新增至節點類型。</span><span class="sxs-lookup"><span data-stu-id="d966c-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="d966c-117">參數</span><span class="sxs-lookup"><span data-stu-id="d966c-117">PARAMETERS</span></span>

### <span data-ttu-id="d966c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d966c-118">-AsJob</span></span>
<span data-ttu-id="d966c-119">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="d966c-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d966c-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d966c-121">指示在部署時間，延伸時是否應使用較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="d966c-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="d966c-122">不過，除非將此屬性設為 true，否則延伸之後就不會升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="d966c-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d966c-123">-ClusterName</span></span>
<span data-ttu-id="d966c-124">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="d966c-124">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d966c-125">-DefaultProfile</span></span>
<span data-ttu-id="d966c-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d966c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="d966c-127">-ForceUpdateTag</span></span>
<span data-ttu-id="d966c-128">如果提供值且與前一個值不同，延伸處理常式將被迫更新，即使延伸設定尚未變更也一樣。</span><span class="sxs-lookup"><span data-stu-id="d966c-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d966c-129">-InputObject</span></span>
<span data-ttu-id="d966c-130">節點類型資源</span><span class="sxs-lookup"><span data-stu-id="d966c-130">Node Type resource</span></span>

```yaml
Type: PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="d966c-131">-Name</span></span>
<span data-ttu-id="d966c-132">副檔名。</span><span class="sxs-lookup"><span data-stu-id="d966c-132">extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="d966c-133">-NodeTypeName</span></span>
<span data-ttu-id="d966c-134">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="d966c-134">Specify the name of the node type.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="d966c-135">-ProtectedSetting</span></span>
<span data-ttu-id="d966c-136">副檔名可以包含 protectedSettings 或 protectedSettingsFromKeyVault，或是根本不包含受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="d966c-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="d966c-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="d966c-138">需要預配此延伸的副檔名名稱集合。</span><span class="sxs-lookup"><span data-stu-id="d966c-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d966c-139">-Publisher</span></span>
<span data-ttu-id="d966c-140">延伸處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="d966c-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="d966c-141">這可以使用 Get-AzVMImagePublisher Cmdlet 來取得發行者。</span><span class="sxs-lookup"><span data-stu-id="d966c-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d966c-142">-ResourceGroupName</span></span>
<span data-ttu-id="d966c-143">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d966c-143">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-144">-設定</span><span class="sxs-lookup"><span data-stu-id="d966c-144">-Setting</span></span>
<span data-ttu-id="d966c-145">副檔名的 Json 格式公開設定。</span><span class="sxs-lookup"><span data-stu-id="d966c-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-146">-類型</span><span class="sxs-lookup"><span data-stu-id="d966c-146">-Type</span></span>
<span data-ttu-id="d966c-147">指定延伸類型;範例是「CustomScriptExtension」。</span><span class="sxs-lookup"><span data-stu-id="d966c-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="d966c-148">您可以使用 Get-AzVMExtensionImageType Cmdlet 來取得延伸類型。</span><span class="sxs-lookup"><span data-stu-id="d966c-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d966c-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="d966c-150">指定腳本處理常式的版本。</span><span class="sxs-lookup"><span data-stu-id="d966c-150">Specifies the version of the script handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-151">-確認</span><span class="sxs-lookup"><span data-stu-id="d966c-151">-Confirm</span></span>
<span data-ttu-id="d966c-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d966c-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d966c-153">-WhatIf</span></span>
<span data-ttu-id="d966c-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d966c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d966c-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d966c-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d966c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d966c-156">CommonParameters</span></span>
<span data-ttu-id="d966c-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d966c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d966c-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d966c-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d966c-159">輸入</span><span class="sxs-lookup"><span data-stu-id="d966c-159">INPUTS</span></span>

### <span data-ttu-id="d966c-160">System.object</span><span class="sxs-lookup"><span data-stu-id="d966c-160">System.String</span></span>

### <span data-ttu-id="d966c-161">PSManagedNodeType 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="d966c-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="d966c-162">輸出</span><span class="sxs-lookup"><span data-stu-id="d966c-162">OUTPUTS</span></span>

### <span data-ttu-id="d966c-163">PSManagedNodeType 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="d966c-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="d966c-164">筆記</span><span class="sxs-lookup"><span data-stu-id="d966c-164">NOTES</span></span>

## <span data-ttu-id="d966c-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="d966c-165">RELATED LINKS</span></span>
