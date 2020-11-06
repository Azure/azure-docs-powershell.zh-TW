---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: d8a795cc27a09fe7b23ac2156115d7a52212e3ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450367"
---
# <span data-ttu-id="842db-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="842db-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="842db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="842db-102">SYNOPSIS</span></span>
<span data-ttu-id="842db-103">建立新的 Analysis Services 伺服器</span><span class="sxs-lookup"><span data-stu-id="842db-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="842db-104">句法</span><span class="sxs-lookup"><span data-stu-id="842db-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="842db-105">說明</span><span class="sxs-lookup"><span data-stu-id="842db-105">DESCRIPTION</span></span>
<span data-ttu-id="842db-106">New-AzureRmAnalysisServicesServer Cmdlet 會建立新的 Analysis Services 伺服器</span><span class="sxs-lookup"><span data-stu-id="842db-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="842db-107">示例</span><span class="sxs-lookup"><span data-stu-id="842db-107">EXAMPLES</span></span>

### <span data-ttu-id="842db-108">範例1</span><span class="sxs-lookup"><span data-stu-id="842db-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="842db-109">在 Azure 地區的 [美國] 和 [資源群組] testresrourcegroup 中建立名為 testserver 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="842db-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="842db-110">伺服器的 sku 層級將是 S1。</span><span class="sxs-lookup"><span data-stu-id="842db-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="842db-111">參數</span><span class="sxs-lookup"><span data-stu-id="842db-111">PARAMETERS</span></span>

### <span data-ttu-id="842db-112">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="842db-112">-Administrator</span></span>
<span data-ttu-id="842db-113">代表要在伺服器上設定為系統管理員之以逗號分隔的使用者或群組清單字串。</span><span class="sxs-lookup"><span data-stu-id="842db-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="842db-114">使用者或群組必須指定 UPN 格式，例如 user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="842db-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="842db-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="842db-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="842db-116">用於備份 Analysis Services 伺服器的 blob 容器 Uri</span><span class="sxs-lookup"><span data-stu-id="842db-116">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="842db-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="842db-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="842db-118">Analysis services 伺服器的預設連接模式</span><span class="sxs-lookup"><span data-stu-id="842db-118">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="842db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="842db-119">-DefaultProfile</span></span>
<span data-ttu-id="842db-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="842db-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842db-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="842db-121">-FirewallConfig</span></span>
<span data-ttu-id="842db-122">分析伺服器的防火牆配置</span><span class="sxs-lookup"><span data-stu-id="842db-122">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="842db-123">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="842db-123">-GatewayResourceId</span></span>
<span data-ttu-id="842db-124">Assocaite 至分析伺服器的閘道資源識別碼</span><span class="sxs-lookup"><span data-stu-id="842db-124">Gateway resource Id for assocaite to an Analysis server</span></span>

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

### <span data-ttu-id="842db-125">-位置</span><span class="sxs-lookup"><span data-stu-id="842db-125">-Location</span></span>
<span data-ttu-id="842db-126">託管分析服務伺服器的 Azure 區域</span><span class="sxs-lookup"><span data-stu-id="842db-126">The Azure region where the Analysis Services server is hosted</span></span>

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

### <span data-ttu-id="842db-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="842db-127">-Name</span></span>
<span data-ttu-id="842db-128">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="842db-128">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="842db-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="842db-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="842db-130">唯讀分析服務伺服器的複本計數</span><span class="sxs-lookup"><span data-stu-id="842db-130">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="842db-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="842db-131">-ResourceGroupName</span></span>
<span data-ttu-id="842db-132">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="842db-132">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="842db-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="842db-133">-Sku</span></span>
<span data-ttu-id="842db-134">伺服器 Sku 的名稱。</span><span class="sxs-lookup"><span data-stu-id="842db-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="842db-135">受支援的值為標準層級的 0 "，" 1 "，" 2 "，"，"2"，"4";[B1 "，" B2 "代表 [基本層]，[中的 1" 代表開發層。</span><span class="sxs-lookup"><span data-stu-id="842db-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="842db-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="842db-136">-Tag</span></span>
<span data-ttu-id="842db-137">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="842db-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="842db-138">-確認</span><span class="sxs-lookup"><span data-stu-id="842db-138">-Confirm</span></span>
<span data-ttu-id="842db-139">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="842db-139">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="842db-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="842db-140">-WhatIf</span></span>
<span data-ttu-id="842db-141">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="842db-141">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="842db-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="842db-142">CommonParameters</span></span>
<span data-ttu-id="842db-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="842db-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="842db-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="842db-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="842db-145">輸入</span><span class="sxs-lookup"><span data-stu-id="842db-145">INPUTS</span></span>

### <span data-ttu-id="842db-146">System.object</span><span class="sxs-lookup"><span data-stu-id="842db-146">System.String</span></span>

### <span data-ttu-id="842db-147">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="842db-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="842db-148">System.object</span><span class="sxs-lookup"><span data-stu-id="842db-148">System.Int32</span></span>

### <span data-ttu-id="842db-149">PsAzureAnalysisServicesFirewallConfig 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="842db-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="842db-150">輸出</span><span class="sxs-lookup"><span data-stu-id="842db-150">OUTPUTS</span></span>

### <span data-ttu-id="842db-151">AzureAnalysisServicesServer 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="842db-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="842db-152">筆記</span><span class="sxs-lookup"><span data-stu-id="842db-152">NOTES</span></span>
<span data-ttu-id="842db-153">別名： New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="842db-153">Alias: New-AzureAs</span></span>

## <span data-ttu-id="842db-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="842db-154">RELATED LINKS</span></span>

[<span data-ttu-id="842db-155">AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="842db-155">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="842db-156">移除-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="842db-156">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
