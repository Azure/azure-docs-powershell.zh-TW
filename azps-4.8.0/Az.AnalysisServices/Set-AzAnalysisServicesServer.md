---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: a3c3338db7fb749b3eb4d5e92c438deda0742a67
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970721"
---
# <span data-ttu-id="c4854-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c4854-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="c4854-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4854-102">SYNOPSIS</span></span>
<span data-ttu-id="c4854-103">修改分析服務伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="c4854-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="c4854-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4854-104">SYNTAX</span></span>

### <span data-ttu-id="c4854-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="c4854-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4854-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="c4854-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4854-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="c4854-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4854-108">說明</span><span class="sxs-lookup"><span data-stu-id="c4854-108">DESCRIPTION</span></span>
<span data-ttu-id="c4854-109">Set-AzAnalysisServicesServer Cmdlet 會修改 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="c4854-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="c4854-110">示例</span><span class="sxs-lookup"><span data-stu-id="c4854-110">EXAMPLES</span></span>

### <span data-ttu-id="c4854-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c4854-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="c4854-112">修改 resourcegroup testgroup 中名為 testserver 的伺服器，將標記設為 key1： value1 和 key2： value2 與 administrator testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="c4854-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="c4854-113">參數</span><span class="sxs-lookup"><span data-stu-id="c4854-113">PARAMETERS</span></span>

### <span data-ttu-id="c4854-114">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="c4854-114">-Administrator</span></span>
<span data-ttu-id="c4854-115">代表要在伺服器上設定為系統管理員之以逗號分隔的使用者或群組清單字串。</span><span class="sxs-lookup"><span data-stu-id="c4854-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="c4854-116">使用者或群組必須指定 UPN 格式，例如 user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="c4854-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="c4854-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="c4854-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="c4854-118">用於備份 Analysis Services 伺服器的 blob 容器 Uri</span><span class="sxs-lookup"><span data-stu-id="c4854-118">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="c4854-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="c4854-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="c4854-120">Analysis services 伺服器的預設連接模式</span><span class="sxs-lookup"><span data-stu-id="c4854-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="c4854-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4854-121">-DefaultProfile</span></span>
<span data-ttu-id="c4854-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4854-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4854-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="c4854-123">-DisableBackup</span></span>
<span data-ttu-id="c4854-124">[切換到停用備份 blob] 容器。</span><span class="sxs-lookup"><span data-stu-id="c4854-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="c4854-125">若要重新啟用備份 blob 容器，請以-BackupBlobContainerUri 提供備份 blob 容器 Uri。</span><span class="sxs-lookup"><span data-stu-id="c4854-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

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

### <span data-ttu-id="c4854-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="c4854-126">-DisassociateGateway</span></span>
<span data-ttu-id="c4854-127">解除分析伺服器與閘道資源的關聯</span><span class="sxs-lookup"><span data-stu-id="c4854-127">Disassociate Gateway resource from an Analysis server</span></span>

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

### <span data-ttu-id="c4854-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="c4854-128">-FirewallConfig</span></span>
<span data-ttu-id="c4854-129">分析伺服器的防火牆配置</span><span class="sxs-lookup"><span data-stu-id="c4854-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="c4854-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c4854-130">-GatewayResourceId</span></span>
<span data-ttu-id="c4854-131">要與分析伺服器關聯的閘道資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c4854-131">Gateway resource Id to associate to an Analysis server</span></span>

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

### <span data-ttu-id="c4854-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="c4854-132">-Name</span></span>
<span data-ttu-id="c4854-133">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="c4854-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="c4854-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4854-134">-PassThru</span></span>
<span data-ttu-id="c4854-135">如果作業成功完成，將會傳回已刪除伺服器的詳細資料</span><span class="sxs-lookup"><span data-stu-id="c4854-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="c4854-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="c4854-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="c4854-137">唯讀分析服務伺服器的複本計數</span><span class="sxs-lookup"><span data-stu-id="c4854-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="c4854-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4854-138">-ResourceGroupName</span></span>
<span data-ttu-id="c4854-139">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="c4854-139">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="c4854-140">-Sku</span><span class="sxs-lookup"><span data-stu-id="c4854-140">-Sku</span></span>
<span data-ttu-id="c4854-141">伺服器 Sku 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4854-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="c4854-142">支援的值為 0 '、' s '、' 2 '、' s '、' s '、' s '、' s '、' s '、' s '、"[B1 "，" B2 "代表 [基本層]，[中的 1" 代表開發層。</span><span class="sxs-lookup"><span data-stu-id="c4854-142">The supported values are 'S0', 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="c4854-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="c4854-143">-Tag</span></span>
<span data-ttu-id="c4854-144">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="c4854-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="c4854-145">-確認</span><span class="sxs-lookup"><span data-stu-id="c4854-145">-Confirm</span></span>
<span data-ttu-id="c4854-146">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="c4854-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="c4854-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4854-147">-WhatIf</span></span>
<span data-ttu-id="c4854-148">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="c4854-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="c4854-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4854-149">CommonParameters</span></span>
<span data-ttu-id="c4854-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4854-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4854-151">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c4854-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4854-152">輸入</span><span class="sxs-lookup"><span data-stu-id="c4854-152">INPUTS</span></span>

### <span data-ttu-id="c4854-153">System.object</span><span class="sxs-lookup"><span data-stu-id="c4854-153">System.String</span></span>

### <span data-ttu-id="c4854-154">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c4854-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c4854-155">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="c4854-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c4854-156">System.object</span><span class="sxs-lookup"><span data-stu-id="c4854-156">System.Int32</span></span>

### <span data-ttu-id="c4854-157">PsAzureAnalysisServicesFirewallConfig 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="c4854-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="c4854-158">輸出</span><span class="sxs-lookup"><span data-stu-id="c4854-158">OUTPUTS</span></span>

### <span data-ttu-id="c4854-159">AzureAnalysisServicesServer 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="c4854-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="c4854-160">筆記</span><span class="sxs-lookup"><span data-stu-id="c4854-160">NOTES</span></span>
<span data-ttu-id="c4854-161">別名： Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="c4854-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="c4854-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4854-162">RELATED LINKS</span></span>

[<span data-ttu-id="c4854-163">AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c4854-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="c4854-164">移除-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c4854-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
