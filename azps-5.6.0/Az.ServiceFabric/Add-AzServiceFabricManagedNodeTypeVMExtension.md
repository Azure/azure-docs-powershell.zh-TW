---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: 14138dddcd4f4b2150377726d862d953c7360a31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906377"
---
# <span data-ttu-id="b5a1b-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="b5a1b-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="b5a1b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b5a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a1b-103">新增 vm 擴充功能至節點類型。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="b5a1b-104">語法</span><span class="sxs-lookup"><span data-stu-id="b5a1b-104">SYNTAX</span></span>

### <span data-ttu-id="b5a1b-105">ByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="b5a1b-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5a1b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b5a1b-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5a1b-107">描述</span><span class="sxs-lookup"><span data-stu-id="b5a1b-107">DESCRIPTION</span></span>
<span data-ttu-id="b5a1b-108">新增 vm 擴充功能至節點類型。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-108">Add vm extension to the node type.</span></span> <span data-ttu-id="b5a1b-109">這會將擴充功能新增到不足的虛擬機器縮放集資源。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="b5a1b-110">例子</span><span class="sxs-lookup"><span data-stu-id="b5a1b-110">EXAMPLES</span></span>

### <span data-ttu-id="b5a1b-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b5a1b-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="b5a1b-112">此命令會將擴充功能新增到節點類型。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="b5a1b-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="b5a1b-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="b5a1b-114">此命令會將具有設定和受保護設定的擴充功能新增到節點類型。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="b5a1b-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="b5a1b-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="b5a1b-116">此命令會將擴充功能新增到節點類型，以及管線。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="b5a1b-117">參數</span><span class="sxs-lookup"><span data-stu-id="b5a1b-117">PARAMETERS</span></span>

### <span data-ttu-id="b5a1b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5a1b-118">-AsJob</span></span>
<span data-ttu-id="b5a1b-119">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b5a1b-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b5a1b-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b5a1b-121">指出擴充功能是否應該使用較新的次要版本 ，如果部署時可以使用該次要版本。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="b5a1b-122">不過，部署後，除非重新部署，即使此屬性設為 True，擴充功能不會升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="b5a1b-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b5a1b-123">-ClusterName</span></span>
<span data-ttu-id="b5a1b-124">指定組名。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b5a1b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a1b-125">-DefaultProfile</span></span>
<span data-ttu-id="b5a1b-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5a1b-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="b5a1b-127">-ForceUpdateTag</span></span>
<span data-ttu-id="b5a1b-128">如果提供值且與先前的值不同，即使擴充功能組配置沒有變更，擴充處理常式也會強制更新。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="b5a1b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5a1b-129">-InputObject</span></span>
<span data-ttu-id="b5a1b-130">節點類型資源</span><span class="sxs-lookup"><span data-stu-id="b5a1b-130">Node Type resource</span></span>

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

### <span data-ttu-id="b5a1b-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5a1b-131">-Name</span></span>
<span data-ttu-id="b5a1b-132">副檔名。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-132">extension name.</span></span>

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

### <span data-ttu-id="b5a1b-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="b5a1b-133">-NodeTypeName</span></span>
<span data-ttu-id="b5a1b-134">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-134">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="b5a1b-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="b5a1b-135">-ProtectedSetting</span></span>
<span data-ttu-id="b5a1b-136">擴充功能可以包含 protectedSettings 或 protectedSettingsFromKeyVault，或完全不包含受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="b5a1b-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="b5a1b-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="b5a1b-138">副檔名集合，之後需要提供此擴充功能。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="b5a1b-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b5a1b-139">-Publisher</span></span>
<span data-ttu-id="b5a1b-140">擴充處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="b5a1b-141">這可以使用 Get-AzVMImagePublisher Cmdlet 取得發行者。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="b5a1b-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5a1b-142">-ResourceGroupName</span></span>
<span data-ttu-id="b5a1b-143">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-143">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b5a1b-144">-設定</span><span class="sxs-lookup"><span data-stu-id="b5a1b-144">-Setting</span></span>
<span data-ttu-id="b5a1b-145">Json 格式化的擴充功能公用設定。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="b5a1b-146">-類型</span><span class="sxs-lookup"><span data-stu-id="b5a1b-146">-Type</span></span>
<span data-ttu-id="b5a1b-147">指定擴充功能的類型;範例為 「CustomScriptExtension」。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="b5a1b-148">您可以使用 Get-AzVMExtensionImageType Cmdlet 取得副檔名類型。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="b5a1b-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b5a1b-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="b5a1b-150">指定腳本處理常式的版本。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-150">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="b5a1b-151">-確認</span><span class="sxs-lookup"><span data-stu-id="b5a1b-151">-Confirm</span></span>
<span data-ttu-id="b5a1b-152">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5a1b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5a1b-153">-WhatIf</span></span>
<span data-ttu-id="b5a1b-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5a1b-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5a1b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a1b-156">CommonParameters</span></span>
<span data-ttu-id="b5a1b-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a1b-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a1b-159">輸入</span><span class="sxs-lookup"><span data-stu-id="b5a1b-159">INPUTS</span></span>

### <span data-ttu-id="b5a1b-160">System.String</span><span class="sxs-lookup"><span data-stu-id="b5a1b-160">System.String</span></span>

### <span data-ttu-id="b5a1b-161">Microsoft.Azure.Commands.ServiceFabric.models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="b5a1b-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="b5a1b-162">輸出</span><span class="sxs-lookup"><span data-stu-id="b5a1b-162">OUTPUTS</span></span>

### <span data-ttu-id="b5a1b-163">Microsoft.Azure.Commands.ServiceFabric.models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="b5a1b-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="b5a1b-164">筆記</span><span class="sxs-lookup"><span data-stu-id="b5a1b-164">NOTES</span></span>

## <span data-ttu-id="b5a1b-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5a1b-165">RELATED LINKS</span></span>
