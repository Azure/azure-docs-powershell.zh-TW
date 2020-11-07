---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
ms.openlocfilehash: 7e6b41a081b5170a34863ff29bf26431224490fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957914"
---
# <span data-ttu-id="f348f-101">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f348f-101">New-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="f348f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f348f-102">SYNOPSIS</span></span>
<span data-ttu-id="f348f-103">建立新的 Analysis Services 伺服器</span><span class="sxs-lookup"><span data-stu-id="f348f-103">Creates a new Analysis Services server</span></span>

## <span data-ttu-id="f348f-104">句法</span><span class="sxs-lookup"><span data-stu-id="f348f-104">SYNTAX</span></span>

```
New-AzAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f348f-105">說明</span><span class="sxs-lookup"><span data-stu-id="f348f-105">DESCRIPTION</span></span>
<span data-ttu-id="f348f-106">New-AzAnalysisServicesServer Cmdlet 會建立新的 Analysis Services 伺服器</span><span class="sxs-lookup"><span data-stu-id="f348f-106">The New-AzAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="f348f-107">示例</span><span class="sxs-lookup"><span data-stu-id="f348f-107">EXAMPLES</span></span>

### <span data-ttu-id="f348f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f348f-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="f348f-109">在 Azure 地區的 [美國] 和 [資源群組] testresourcegroup 中建立名為 testserver 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="f348f-109">Creates a server named testserver in the Azure region West-US and in resource group testresourcegroup.</span></span> <span data-ttu-id="f348f-110">伺服器的 sku 層級將是 S1。</span><span class="sxs-lookup"><span data-stu-id="f348f-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="f348f-111">參數</span><span class="sxs-lookup"><span data-stu-id="f348f-111">PARAMETERS</span></span>

### <span data-ttu-id="f348f-112">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="f348f-112">-Administrator</span></span>
<span data-ttu-id="f348f-113">代表要在伺服器上設定為系統管理員之以逗號分隔的使用者或群組清單字串。</span><span class="sxs-lookup"><span data-stu-id="f348f-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="f348f-114">使用者或群組必須指定 UPN 格式，例如 user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f348f-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f348f-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="f348f-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="f348f-116">用於備份 Analysis Services 伺服器的 blob 容器 Uri</span><span class="sxs-lookup"><span data-stu-id="f348f-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f348f-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="f348f-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="f348f-118">Analysis services 伺服器的預設連接模式</span><span class="sxs-lookup"><span data-stu-id="f348f-118">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="f348f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f348f-119">-DefaultProfile</span></span>
<span data-ttu-id="f348f-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f348f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f348f-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="f348f-121">-FirewallConfig</span></span>
<span data-ttu-id="f348f-122">分析伺服器的防火牆配置</span><span class="sxs-lookup"><span data-stu-id="f348f-122">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="f348f-123">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="f348f-123">-GatewayResourceId</span></span>
<span data-ttu-id="f348f-124">要與分析伺服器關聯的閘道資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f348f-124">Gateway resource Id to associate to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f348f-125">-位置</span><span class="sxs-lookup"><span data-stu-id="f348f-125">-Location</span></span>
<span data-ttu-id="f348f-126">託管分析服務伺服器的 Azure 區域</span><span class="sxs-lookup"><span data-stu-id="f348f-126">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f348f-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="f348f-127">-Name</span></span>
<span data-ttu-id="f348f-128">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="f348f-128">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f348f-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="f348f-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="f348f-130">唯讀分析服務伺服器的複本計數</span><span class="sxs-lookup"><span data-stu-id="f348f-130">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="f348f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f348f-131">-ResourceGroupName</span></span>
<span data-ttu-id="f348f-132">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="f348f-132">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="f348f-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="f348f-133">-Sku</span></span>
<span data-ttu-id="f348f-134">伺服器 Sku 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f348f-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="f348f-135">受支援的值為標準層級的 0 "，" 1 "，" 2 "，"，"2"，"4";[B1 "，" B2 "代表 [基本層]，[中的 1" 代表開發層。</span><span class="sxs-lookup"><span data-stu-id="f348f-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f348f-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="f348f-136">-Tag</span></span>
<span data-ttu-id="f348f-137">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="f348f-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f348f-138">-確認</span><span class="sxs-lookup"><span data-stu-id="f348f-138">-Confirm</span></span>
<span data-ttu-id="f348f-139">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="f348f-139">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="f348f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f348f-140">-WhatIf</span></span>
<span data-ttu-id="f348f-141">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="f348f-141">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="f348f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f348f-142">CommonParameters</span></span>
<span data-ttu-id="f348f-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f348f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f348f-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f348f-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f348f-145">輸入</span><span class="sxs-lookup"><span data-stu-id="f348f-145">INPUTS</span></span>

### <span data-ttu-id="f348f-146">System.object</span><span class="sxs-lookup"><span data-stu-id="f348f-146">System.String</span></span>

### <span data-ttu-id="f348f-147">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f348f-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f348f-148">System.object</span><span class="sxs-lookup"><span data-stu-id="f348f-148">System.Int32</span></span>

### <span data-ttu-id="f348f-149">PsAzureAnalysisServicesFirewallConfig 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="f348f-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="f348f-150">輸出</span><span class="sxs-lookup"><span data-stu-id="f348f-150">OUTPUTS</span></span>

### <span data-ttu-id="f348f-151">AzureAnalysisServicesServer 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="f348f-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="f348f-152">筆記</span><span class="sxs-lookup"><span data-stu-id="f348f-152">NOTES</span></span>
<span data-ttu-id="f348f-153">別名： New-AzAs</span><span class="sxs-lookup"><span data-stu-id="f348f-153">Alias: New-AzAs</span></span>

## <span data-ttu-id="f348f-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="f348f-154">RELATED LINKS</span></span>

[<span data-ttu-id="f348f-155">AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f348f-155">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="f348f-156">移除-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f348f-156">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
