---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 6bda63ad0c8e900a73c0ccd2afc506be7feae908
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445248"
---
# <span data-ttu-id="52c46-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="52c46-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="52c46-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52c46-102">SYNOPSIS</span></span>
<span data-ttu-id="52c46-103">修改分析服務伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="52c46-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52c46-104">句法</span><span class="sxs-lookup"><span data-stu-id="52c46-104">SYNTAX</span></span>

### <span data-ttu-id="52c46-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="52c46-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52c46-106">停用備份</span><span class="sxs-lookup"><span data-stu-id="52c46-106">Disable Backup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52c46-107">說明</span><span class="sxs-lookup"><span data-stu-id="52c46-107">DESCRIPTION</span></span>
<span data-ttu-id="52c46-108">Set-AzureRmAnalysisServicesServer Cmdlet 會修改 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="52c46-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="52c46-109">示例</span><span class="sxs-lookup"><span data-stu-id="52c46-109">EXAMPLES</span></span>

### <span data-ttu-id="52c46-110">範例1</span><span class="sxs-lookup"><span data-stu-id="52c46-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="52c46-111">修改 resourcegroup testgroup 中名為 testserver 的伺服器，將標記設為 key1： value1 和 key2： value2 與 administrator testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="52c46-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="52c46-112">參數</span><span class="sxs-lookup"><span data-stu-id="52c46-112">PARAMETERS</span></span>

### <span data-ttu-id="52c46-113">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="52c46-113">-Administrator</span></span>
<span data-ttu-id="52c46-114">代表要在伺服器上設定為系統管理員之以逗號分隔的使用者或群組清單字串。</span><span class="sxs-lookup"><span data-stu-id="52c46-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="52c46-115">使用者或群組必須指定 UPN 格式，例如 user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="52c46-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="52c46-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="52c46-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="52c46-117">用於備份 Analysis Services 伺服器的 blob 容器 Uri</span><span class="sxs-lookup"><span data-stu-id="52c46-117">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="52c46-118">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="52c46-118">-DisableBackup</span></span>
<span data-ttu-id="52c46-119">[切換到停用備份 blob] 容器。</span><span class="sxs-lookup"><span data-stu-id="52c46-119">The switch to disable backup blob container.</span></span>
<span data-ttu-id="52c46-120">若要重新啟用備份 blob 容器，請以-BackupBlobContainerUri 提供備份 blob 容器 Uri。</span><span class="sxs-lookup"><span data-stu-id="52c46-120">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Backup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52c46-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="52c46-121">-Name</span></span>
<span data-ttu-id="52c46-122">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="52c46-122">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="52c46-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52c46-123">-PassThru</span></span>
<span data-ttu-id="52c46-124">如果作業成功完成，將會傳回已刪除伺服器的詳細資料</span><span class="sxs-lookup"><span data-stu-id="52c46-124">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="52c46-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52c46-125">-ResourceGroupName</span></span>
<span data-ttu-id="52c46-126">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="52c46-126">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="52c46-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="52c46-127">-Sku</span></span>
<span data-ttu-id="52c46-128">伺服器 Sku 的名稱。</span><span class="sxs-lookup"><span data-stu-id="52c46-128">The name of the Sku for the server.</span></span>
<span data-ttu-id="52c46-129">受支援的值為標準層級的 0 "，" 1 "，" 2 "，"，"2"，"4";[B1 "，" B2 "代表 [基本層]，[中的 1" 代表開發層。</span><span class="sxs-lookup"><span data-stu-id="52c46-129">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="52c46-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="52c46-130">-Tag</span></span>
<span data-ttu-id="52c46-131">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="52c46-131">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="52c46-132">-確認</span><span class="sxs-lookup"><span data-stu-id="52c46-132">-Confirm</span></span>
<span data-ttu-id="52c46-133">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="52c46-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="52c46-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52c46-134">-WhatIf</span></span>
<span data-ttu-id="52c46-135">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="52c46-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="52c46-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52c46-136">-DefaultProfile</span></span>
<span data-ttu-id="52c46-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52c46-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52c46-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c46-138">CommonParameters</span></span>
<span data-ttu-id="52c46-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52c46-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c46-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52c46-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c46-141">輸入</span><span class="sxs-lookup"><span data-stu-id="52c46-141">INPUTS</span></span>

## <span data-ttu-id="52c46-142">輸出</span><span class="sxs-lookup"><span data-stu-id="52c46-142">OUTPUTS</span></span>

### <span data-ttu-id="52c46-143">AnalysisServicesServer 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="52c46-143">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="52c46-144">筆記</span><span class="sxs-lookup"><span data-stu-id="52c46-144">NOTES</span></span>
<span data-ttu-id="52c46-145">別名： Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="52c46-145">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="52c46-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="52c46-146">RELATED LINKS</span></span>

[<span data-ttu-id="52c46-147">AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="52c46-147">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="52c46-148">移除-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="52c46-148">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
