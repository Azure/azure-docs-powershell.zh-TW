---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: 81a50a8c805d05b47b934b899eff708031ac6beb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137564"
---
# <span data-ttu-id="74ca3-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="74ca3-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="74ca3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="74ca3-103">取得從 DSC 節點傳送到自動化的報表。</span><span class="sxs-lookup"><span data-stu-id="74ca3-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="74ca3-104">句法</span><span class="sxs-lookup"><span data-stu-id="74ca3-104">SYNTAX</span></span>

### <span data-ttu-id="74ca3-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="74ca3-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74ca3-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="74ca3-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74ca3-107">ById</span><span class="sxs-lookup"><span data-stu-id="74ca3-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74ca3-108">說明</span><span class="sxs-lookup"><span data-stu-id="74ca3-108">DESCRIPTION</span></span>
<span data-ttu-id="74ca3-109">**AzAutomationDscNodeReport** Cmdlet 會從傳送所需的接入件人狀態設定傳送報告至 Azure 自動化 (DSC) 節點。</span><span class="sxs-lookup"><span data-stu-id="74ca3-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="74ca3-110">示例</span><span class="sxs-lookup"><span data-stu-id="74ca3-110">EXAMPLES</span></span>

### <span data-ttu-id="74ca3-111">範例1：取得 DSC 節點的所有報表</span><span class="sxs-lookup"><span data-stu-id="74ca3-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="74ca3-112">第一個命令會取得名為 Contoso17 之自動化帳戶中名為 Computer14 的電腦的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="74ca3-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="74ca3-113">該命令會將這個物件儲存在 $Node 變數中。</span><span class="sxs-lookup"><span data-stu-id="74ca3-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="74ca3-114">第二個命令會從名為 Computer14 的 DSC 節點傳送到名為 Contoso17 的自動化帳戶的所有報表，取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="74ca3-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="74ca3-115">命令會使用 $Node 物件的 **識別碼** 屬性來指定節點。</span><span class="sxs-lookup"><span data-stu-id="74ca3-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="74ca3-116">範例2：依報表識別碼取得 DSC 節點的報表</span><span class="sxs-lookup"><span data-stu-id="74ca3-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="74ca3-117">第一個命令會取得名為 Contoso17 之自動化帳戶中名為 Computer14 的電腦的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="74ca3-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="74ca3-118">該命令會將這個物件儲存在 $Node 變數中。</span><span class="sxs-lookup"><span data-stu-id="74ca3-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="74ca3-119">第二個命令會針對從名為 Computer14 的 DSC 節點傳送給名為 Contoso17 之自動化帳戶的指定識別碼所標識的報表，取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="74ca3-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="74ca3-120">範例3：取得 DSC 節點的最新報表</span><span class="sxs-lookup"><span data-stu-id="74ca3-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="74ca3-121">第一個命令會取得名為 Contoso17 之自動化帳戶中名為 Computer14 的電腦的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="74ca3-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="74ca3-122">該命令會將這個物件儲存在 $Node 變數中。</span><span class="sxs-lookup"><span data-stu-id="74ca3-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="74ca3-123">第二個命令會針對從名為 Computer14 的 DSC 節點傳送到名為 Contoso17 的自動化帳戶的最新報表，取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="74ca3-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="74ca3-124">參數</span><span class="sxs-lookup"><span data-stu-id="74ca3-124">PARAMETERS</span></span>

### <span data-ttu-id="74ca3-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="74ca3-125">-AutomationAccountName</span></span>
<span data-ttu-id="74ca3-126">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="74ca3-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="74ca3-127">這個 Cmdlet 會匯出屬於此參數所指定帳戶的 DSC 節點報告。</span><span class="sxs-lookup"><span data-stu-id="74ca3-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="74ca3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ca3-128">-DefaultProfile</span></span>
<span data-ttu-id="74ca3-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="74ca3-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74ca3-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="74ca3-130">-EndTime</span></span>
<span data-ttu-id="74ca3-131">指定結束時間。</span><span class="sxs-lookup"><span data-stu-id="74ca3-131">Specifies an end time.</span></span>
<span data-ttu-id="74ca3-132">這個 Cmdlet 會取得此時間之前接收到的自動報告。</span><span class="sxs-lookup"><span data-stu-id="74ca3-132">This cmdlet gets reports that Automation received before this time.</span></span>

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

### <span data-ttu-id="74ca3-133">-識別碼</span><span class="sxs-lookup"><span data-stu-id="74ca3-133">-Id</span></span>
<span data-ttu-id="74ca3-134">指定此 Cmdlet 要取得的 DSC 節點報告的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="74ca3-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

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

### <span data-ttu-id="74ca3-135">-最新</span><span class="sxs-lookup"><span data-stu-id="74ca3-135">-Latest</span></span>
<span data-ttu-id="74ca3-136">表示此 Cmdlet 只會取得指定節點的最新 DSC 報告。</span><span class="sxs-lookup"><span data-stu-id="74ca3-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

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

### <span data-ttu-id="74ca3-137">-</span><span class="sxs-lookup"><span data-stu-id="74ca3-137">-NodeId</span></span>
<span data-ttu-id="74ca3-138">指定此 Cmdlet 取得報告之 DSC 節點的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="74ca3-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="74ca3-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74ca3-139">-ResourceGroupName</span></span>
<span data-ttu-id="74ca3-140">指定包含此 Cmdlet 取得報告之 DSC 節點之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="74ca3-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="74ca3-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="74ca3-141">-StartTime</span></span>
<span data-ttu-id="74ca3-142">指定開始時間。</span><span class="sxs-lookup"><span data-stu-id="74ca3-142">Specifies a start time.</span></span>
<span data-ttu-id="74ca3-143">這個 Cmdlet 會取得此時間之後自動接收的報告。</span><span class="sxs-lookup"><span data-stu-id="74ca3-143">This cmdlet gets reports that Automation received after this time.</span></span>

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

### <span data-ttu-id="74ca3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ca3-144">CommonParameters</span></span>
<span data-ttu-id="74ca3-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74ca3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74ca3-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74ca3-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ca3-147">輸入</span><span class="sxs-lookup"><span data-stu-id="74ca3-147">INPUTS</span></span>

### <span data-ttu-id="74ca3-148">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="74ca3-148">System.Guid</span></span>

### <span data-ttu-id="74ca3-149">"CoreLib" 1 [（System.object，System.object，，版本 = 4.0.0.0，Culture = 中立，</span><span class="sxs-lookup"><span data-stu-id="74ca3-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="74ca3-150">System.object</span><span class="sxs-lookup"><span data-stu-id="74ca3-150">System.String</span></span>

## <span data-ttu-id="74ca3-151">輸出</span><span class="sxs-lookup"><span data-stu-id="74ca3-151">OUTPUTS</span></span>

### <span data-ttu-id="74ca3-152">DscNode 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="74ca3-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="74ca3-153">筆記</span><span class="sxs-lookup"><span data-stu-id="74ca3-153">NOTES</span></span>

## <span data-ttu-id="74ca3-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="74ca3-154">RELATED LINKS</span></span>

[<span data-ttu-id="74ca3-155">AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="74ca3-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="74ca3-156">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="74ca3-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


