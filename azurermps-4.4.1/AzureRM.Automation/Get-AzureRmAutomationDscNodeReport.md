---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: c3ae9da7959d606ec8ab92ed7a05e502d03b12a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450081"
---
# <span data-ttu-id="02c49-101">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="02c49-101">Get-AzureRmAutomationDscNodeReport</span></span>

## <span data-ttu-id="02c49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02c49-102">SYNOPSIS</span></span>
<span data-ttu-id="02c49-103">取得從 DSC 節點傳送到自動化的報表。</span><span class="sxs-lookup"><span data-stu-id="02c49-103">Gets reports sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02c49-104">句法</span><span class="sxs-lookup"><span data-stu-id="02c49-104">SYNTAX</span></span>

### <span data-ttu-id="02c49-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="02c49-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02c49-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="02c49-106">ByLatest</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02c49-107">ById</span><span class="sxs-lookup"><span data-stu-id="02c49-107">ById</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02c49-108">說明</span><span class="sxs-lookup"><span data-stu-id="02c49-108">DESCRIPTION</span></span>
<span data-ttu-id="02c49-109">**AzureRmAutomationDscNodeReport** Cmdlet 會從傳送所需的接入件人狀態設定傳送報告至 Azure 自動化 (DSC) 節點。</span><span class="sxs-lookup"><span data-stu-id="02c49-109">The **Get-AzureRmAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="02c49-110">示例</span><span class="sxs-lookup"><span data-stu-id="02c49-110">EXAMPLES</span></span>

### <span data-ttu-id="02c49-111">範例1：取得 DSC 節點的所有報表</span><span class="sxs-lookup"><span data-stu-id="02c49-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="02c49-112">第一個命令會取得名為 Contoso17 之自動化帳戶中名為 Computer14 的電腦的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="02c49-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="02c49-113">該命令會將這個物件儲存在 $Node 變數中。</span><span class="sxs-lookup"><span data-stu-id="02c49-113">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="02c49-114">第二個命令會從名為 Computer14 的 DSC 節點傳送到名為 Contoso17 的自動化帳戶的所有報表，取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="02c49-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="02c49-115">命令會使用 $Node 物件的 **識別碼** 屬性來指定節點。</span><span class="sxs-lookup"><span data-stu-id="02c49-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="02c49-116">範例2：依報表識別碼取得 DSC 節點的報表</span><span class="sxs-lookup"><span data-stu-id="02c49-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="02c49-117">第一個命令會取得名為 Contoso17 之自動化帳戶中名為 Computer14 的電腦的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="02c49-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="02c49-118">該命令會將這個物件儲存在 $Node 變數中。</span><span class="sxs-lookup"><span data-stu-id="02c49-118">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="02c49-119">第二個命令會針對從名為 Computer14 的 DSC 節點傳送給名為 Contoso17 之自動化帳戶的指定識別碼所標識的報表，取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="02c49-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="02c49-120">範例3：取得 DSC 節點的最新報表</span><span class="sxs-lookup"><span data-stu-id="02c49-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="02c49-121">第一個命令會取得名為 Contoso17 之自動化帳戶中名為 Computer14 的電腦的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="02c49-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="02c49-122">該命令會將這個物件儲存在 $Node 變數中。</span><span class="sxs-lookup"><span data-stu-id="02c49-122">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="02c49-123">第二個命令會針對從名為 Computer14 的 DSC 節點傳送到名為 Contoso17 的自動化帳戶的最新報表，取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="02c49-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="02c49-124">參數</span><span class="sxs-lookup"><span data-stu-id="02c49-124">PARAMETERS</span></span>

### <span data-ttu-id="02c49-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="02c49-125">-AutomationAccountName</span></span>
<span data-ttu-id="02c49-126">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="02c49-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="02c49-127">這個 Cmdlet 會匯出屬於此參數所指定帳戶的 DSC 節點報告。</span><span class="sxs-lookup"><span data-stu-id="02c49-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="02c49-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="02c49-128">-EndTime</span></span>
<span data-ttu-id="02c49-129">指定結束時間。</span><span class="sxs-lookup"><span data-stu-id="02c49-129">Specifies an end time.</span></span>
<span data-ttu-id="02c49-130">這個 Cmdlet 會取得此時間之前接收到的自動報告。</span><span class="sxs-lookup"><span data-stu-id="02c49-130">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c49-131">-識別碼</span><span class="sxs-lookup"><span data-stu-id="02c49-131">-Id</span></span>
<span data-ttu-id="02c49-132">指定此 Cmdlet 要取得的 DSC 節點報告的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="02c49-132">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c49-133">-最新</span><span class="sxs-lookup"><span data-stu-id="02c49-133">-Latest</span></span>
<span data-ttu-id="02c49-134">表示此 Cmdlet 只會取得指定節點的最新 DSC 報告。</span><span class="sxs-lookup"><span data-stu-id="02c49-134">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c49-135">-</span><span class="sxs-lookup"><span data-stu-id="02c49-135">-NodeId</span></span>
<span data-ttu-id="02c49-136">指定此 Cmdlet 取得報告之 DSC 節點的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="02c49-136">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c49-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c49-137">-ResourceGroupName</span></span>
<span data-ttu-id="02c49-138">指定包含此 Cmdlet 取得報告之 DSC 節點之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="02c49-138">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="02c49-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="02c49-139">-StartTime</span></span>
<span data-ttu-id="02c49-140">指定開始時間。</span><span class="sxs-lookup"><span data-stu-id="02c49-140">Specifies a start time.</span></span>
<span data-ttu-id="02c49-141">這個 Cmdlet 會取得此時間之後自動接收的報告。</span><span class="sxs-lookup"><span data-stu-id="02c49-141">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c49-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c49-142">-DefaultProfile</span></span>
<span data-ttu-id="02c49-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="02c49-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02c49-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c49-144">CommonParameters</span></span>
<span data-ttu-id="02c49-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02c49-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c49-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02c49-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c49-147">輸入</span><span class="sxs-lookup"><span data-stu-id="02c49-147">INPUTS</span></span>

## <span data-ttu-id="02c49-148">輸出</span><span class="sxs-lookup"><span data-stu-id="02c49-148">OUTPUTS</span></span>

### <span data-ttu-id="02c49-149">DscNode 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="02c49-149">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="02c49-150">筆記</span><span class="sxs-lookup"><span data-stu-id="02c49-150">NOTES</span></span>

## <span data-ttu-id="02c49-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="02c49-151">RELATED LINKS</span></span>

[<span data-ttu-id="02c49-152">AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="02c49-152">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="02c49-153">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="02c49-153">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)


