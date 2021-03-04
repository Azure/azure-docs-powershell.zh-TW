---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: b39da37f41e3a18bc70f25fe36d67301e49867c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903749"
---
# <span data-ttu-id="85d40-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="85d40-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="85d40-102">簡介</span><span class="sxs-lookup"><span data-stu-id="85d40-102">SYNOPSIS</span></span>
<span data-ttu-id="85d40-103">修改 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="85d40-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="85d40-104">語法</span><span class="sxs-lookup"><span data-stu-id="85d40-104">SYNTAX</span></span>

### <span data-ttu-id="85d40-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="85d40-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85d40-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="85d40-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85d40-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="85d40-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85d40-108">描述</span><span class="sxs-lookup"><span data-stu-id="85d40-108">DESCRIPTION</span></span>
<span data-ttu-id="85d40-109">此Set-AzAnalysisServicesServer Cmdlet 會修改 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="85d40-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="85d40-110">例子</span><span class="sxs-lookup"><span data-stu-id="85d40-110">EXAMPLES</span></span>

### <span data-ttu-id="85d40-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="85d40-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="85d40-112">修改資源組測試組中名為 testerver 的伺服器，將標記設為 key1：value1 和 key2：value2，以及系統管理員 testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="85d40-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="85d40-113">參數</span><span class="sxs-lookup"><span data-stu-id="85d40-113">PARAMETERS</span></span>

### <span data-ttu-id="85d40-114">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="85d40-114">-Administrator</span></span>
<span data-ttu-id="85d40-115">代表要設定為伺服器上系統管理員之使用者或群組之逗號分隔清單的字串。</span><span class="sxs-lookup"><span data-stu-id="85d40-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="85d40-116">使用者或群組必須指定 UPN 格式，例如 user@contoso.com ，或 groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="85d40-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d40-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="85d40-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="85d40-118">用於備份 Analysis Services 伺服器的 Blob 容器 Uri</span><span class="sxs-lookup"><span data-stu-id="85d40-118">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d40-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="85d40-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="85d40-120">Analysis 服務伺服器的預設連接模式</span><span class="sxs-lookup"><span data-stu-id="85d40-120">Default connection mode of an Analysis service server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d40-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85d40-121">-DefaultProfile</span></span>
<span data-ttu-id="85d40-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="85d40-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85d40-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="85d40-123">-DisableBackup</span></span>
<span data-ttu-id="85d40-124">停用備份 Blob 容器的開關。</span><span class="sxs-lookup"><span data-stu-id="85d40-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="85d40-125">若要重新啟用備份 Blob 容器，請提供備份 Blob 容器 Uri 做為 -BackupBlobContainerUri。</span><span class="sxs-lookup"><span data-stu-id="85d40-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBackup
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d40-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="85d40-126">-DisassociateGateway</span></span>
<span data-ttu-id="85d40-127">解除關聯分析伺服器的閘道資源</span><span class="sxs-lookup"><span data-stu-id="85d40-127">Disassociate Gateway resource from an Analysis server</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisassociateGateway
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d40-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="85d40-128">-FirewallConfig</span></span>
<span data-ttu-id="85d40-129">分析伺服器的防火牆設定檔</span><span class="sxs-lookup"><span data-stu-id="85d40-129">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d40-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="85d40-130">-GatewayResourceId</span></span>
<span data-ttu-id="85d40-131">要與分析伺服器建立關聯的閘道資源識別碼</span><span class="sxs-lookup"><span data-stu-id="85d40-131">Gateway resource Id to associate to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d40-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="85d40-132">-Name</span></span>
<span data-ttu-id="85d40-133">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="85d40-133">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d40-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85d40-134">-PassThru</span></span>
<span data-ttu-id="85d40-135">如果作業順利完成，會返回已刪除的伺服器詳細資料</span><span class="sxs-lookup"><span data-stu-id="85d40-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="85d40-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="85d40-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="85d40-137">Analysis 服務伺服器的唯讀複本計數</span><span class="sxs-lookup"><span data-stu-id="85d40-137">Read only replica count of an Analysis service server</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d40-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85d40-138">-ResourceGroupName</span></span>
<span data-ttu-id="85d40-139">伺服器所屬的 Azure 資源組名</span><span class="sxs-lookup"><span data-stu-id="85d40-139">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d40-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="85d40-140">-Sku</span></span>
<span data-ttu-id="85d40-141">伺服器 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="85d40-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="85d40-142">支援的值為標準層級的 'S0'、'S1'、'S2'、'S4'、'S8'、'S9'、'S8v2'、'S9v2';基本層級為 'B1'、'B2' 和 'D1' 表示開發層。</span><span class="sxs-lookup"><span data-stu-id="85d40-142">The supported values are 'S0', 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d40-143">-標記</span><span class="sxs-lookup"><span data-stu-id="85d40-143">-Tag</span></span>
<span data-ttu-id="85d40-144">以雜湊表格形式設定為伺服器上標記的索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="85d40-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d40-145">-確認</span><span class="sxs-lookup"><span data-stu-id="85d40-145">-Confirm</span></span>
<span data-ttu-id="85d40-146">提示使用者確認是否要執行作業</span><span class="sxs-lookup"><span data-stu-id="85d40-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="85d40-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85d40-147">-WhatIf</span></span>
<span data-ttu-id="85d40-148">說明目前作業不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="85d40-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="85d40-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85d40-149">CommonParameters</span></span>
<span data-ttu-id="85d40-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="85d40-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85d40-151">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="85d40-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85d40-152">輸入</span><span class="sxs-lookup"><span data-stu-id="85d40-152">INPUTS</span></span>

### <span data-ttu-id="85d40-153">System.String</span><span class="sxs-lookup"><span data-stu-id="85d40-153">System.String</span></span>

### <span data-ttu-id="85d40-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="85d40-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="85d40-155">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="85d40-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="85d40-156">System.Int32</span><span class="sxs-lookup"><span data-stu-id="85d40-156">System.Int32</span></span>

### <span data-ttu-id="85d40-157">Microsoft.Azure.Commands.AnalysisServices.models.PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="85d40-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="85d40-158">輸出</span><span class="sxs-lookup"><span data-stu-id="85d40-158">OUTPUTS</span></span>

### <span data-ttu-id="85d40-159">Microsoft.Azure.Commands.AnalysisServices.models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="85d40-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="85d40-160">筆記</span><span class="sxs-lookup"><span data-stu-id="85d40-160">NOTES</span></span>
<span data-ttu-id="85d40-161">別名：Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="85d40-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="85d40-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="85d40-162">RELATED LINKS</span></span>

[<span data-ttu-id="85d40-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="85d40-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="85d40-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="85d40-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
