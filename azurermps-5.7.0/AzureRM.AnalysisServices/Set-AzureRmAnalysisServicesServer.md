---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/set-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 485687b0a08ca69edc77b4ee5f9510ad8a1396a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447103"
---
# <span data-ttu-id="26f66-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="26f66-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="26f66-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26f66-102">SYNOPSIS</span></span>
<span data-ttu-id="26f66-103">修改分析服務伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="26f66-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26f66-104">句法</span><span class="sxs-lookup"><span data-stu-id="26f66-104">SYNTAX</span></span>

### <span data-ttu-id="26f66-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="26f66-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26f66-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="26f66-106">DisableBackup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26f66-107">說明</span><span class="sxs-lookup"><span data-stu-id="26f66-107">DESCRIPTION</span></span>
<span data-ttu-id="26f66-108">Set-AzureRmAnalysisServicesServer Cmdlet 會修改 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="26f66-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="26f66-109">示例</span><span class="sxs-lookup"><span data-stu-id="26f66-109">EXAMPLES</span></span>

### <span data-ttu-id="26f66-110">範例1</span><span class="sxs-lookup"><span data-stu-id="26f66-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="26f66-111">修改 resourcegroup testgroup 中名為 testserver 的伺服器，將標記設為 key1： value1 和 key2： value2 與 administrator testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="26f66-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="26f66-112">參數</span><span class="sxs-lookup"><span data-stu-id="26f66-112">PARAMETERS</span></span>

### <span data-ttu-id="26f66-113">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="26f66-113">-Administrator</span></span>
<span data-ttu-id="26f66-114">代表要在伺服器上設定為系統管理員之以逗號分隔的使用者或群組清單字串。</span><span class="sxs-lookup"><span data-stu-id="26f66-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="26f66-115">使用者或群組必須指定 UPN 格式，例如 user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="26f66-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f66-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="26f66-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="26f66-117">用於備份 Analysis Services 伺服器的 blob 容器 Uri</span><span class="sxs-lookup"><span data-stu-id="26f66-117">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f66-118">-DefaultProfile</span></span>
<span data-ttu-id="26f66-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26f66-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f66-120">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="26f66-120">-DisableBackup</span></span>
<span data-ttu-id="26f66-121">[切換到停用備份 blob] 容器。</span><span class="sxs-lookup"><span data-stu-id="26f66-121">The switch to disable backup blob container.</span></span>
<span data-ttu-id="26f66-122">若要重新啟用備份 blob 容器，請以-BackupBlobContainerUri 提供備份 blob 容器 Uri。</span><span class="sxs-lookup"><span data-stu-id="26f66-122">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBackup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f66-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="26f66-123">-Name</span></span>
<span data-ttu-id="26f66-124">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="26f66-124">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f66-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26f66-125">-PassThru</span></span>
<span data-ttu-id="26f66-126">如果作業成功完成，將會傳回已刪除伺服器的詳細資料</span><span class="sxs-lookup"><span data-stu-id="26f66-126">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="26f66-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f66-127">-ResourceGroupName</span></span>
<span data-ttu-id="26f66-128">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="26f66-128">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f66-129">-Sku</span><span class="sxs-lookup"><span data-stu-id="26f66-129">-Sku</span></span>
<span data-ttu-id="26f66-130">伺服器 Sku 的名稱。</span><span class="sxs-lookup"><span data-stu-id="26f66-130">The name of the Sku for the server.</span></span>
<span data-ttu-id="26f66-131">受支援的值為標準層級的 0 "，" 1 "，" 2 "，"，"2"，"4";[B1 "，" B2 "代表 [基本層]，[中的 1" 代表開發層。</span><span class="sxs-lookup"><span data-stu-id="26f66-131">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f66-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="26f66-132">-Tag</span></span>
<span data-ttu-id="26f66-133">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="26f66-133">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f66-134">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="26f66-134">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="26f66-135">唯讀分析服務伺服器的複本計數</span><span class="sxs-lookup"><span data-stu-id="26f66-135">Read only replica count of an Analysis service server</span></span>

```yaml
Type: Integer
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f66-136">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="26f66-136">-DefaultConnectionMode</span></span>
<span data-ttu-id="26f66-137">Analysis services 伺服器的預設連接模式</span><span class="sxs-lookup"><span data-stu-id="26f66-137">Default connection mode of an Analysis service server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f66-138">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="26f66-138">-FirewallConfig</span></span>
<span data-ttu-id="26f66-139">分析伺服器的防火牆配置</span><span class="sxs-lookup"><span data-stu-id="26f66-139">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f66-140">-確認</span><span class="sxs-lookup"><span data-stu-id="26f66-140">-Confirm</span></span>
<span data-ttu-id="26f66-141">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="26f66-141">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="26f66-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26f66-142">-WhatIf</span></span>
<span data-ttu-id="26f66-143">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="26f66-143">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="26f66-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f66-144">CommonParameters</span></span>
<span data-ttu-id="26f66-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26f66-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f66-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26f66-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f66-147">輸入</span><span class="sxs-lookup"><span data-stu-id="26f66-147">INPUTS</span></span>

### <span data-ttu-id="26f66-148">所有</span><span class="sxs-lookup"><span data-stu-id="26f66-148">None</span></span>
<span data-ttu-id="26f66-149">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="26f66-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26f66-150">輸出</span><span class="sxs-lookup"><span data-stu-id="26f66-150">OUTPUTS</span></span>

### <span data-ttu-id="26f66-151">AnalysisServicesServer 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="26f66-151">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="26f66-152">筆記</span><span class="sxs-lookup"><span data-stu-id="26f66-152">NOTES</span></span>
<span data-ttu-id="26f66-153">別名： Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="26f66-153">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="26f66-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="26f66-154">RELATED LINKS</span></span>

[<span data-ttu-id="26f66-155">AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="26f66-155">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="26f66-156">移除-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="26f66-156">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
