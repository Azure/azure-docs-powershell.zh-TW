---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: bb88bc38f6102f18b4d45b3b80902886975e2628
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910781"
---
# <span data-ttu-id="92509-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="92509-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="92509-102">簡介</span><span class="sxs-lookup"><span data-stu-id="92509-102">SYNOPSIS</span></span>
<span data-ttu-id="92509-103">從 DSC 節點將報表送往自動化。</span><span class="sxs-lookup"><span data-stu-id="92509-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="92509-104">語法</span><span class="sxs-lookup"><span data-stu-id="92509-104">SYNTAX</span></span>

### <span data-ttu-id="92509-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="92509-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92509-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="92509-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92509-107">ById</span><span class="sxs-lookup"><span data-stu-id="92509-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92509-108">描述</span><span class="sxs-lookup"><span data-stu-id="92509-108">DESCRIPTION</span></span>
<span data-ttu-id="92509-109">**Get-AzAutomationDscNodeReport** Cmdlet 會從 APS 想要的狀態組態 (DSC) 節點傳送報表至 Azure Automation。</span><span class="sxs-lookup"><span data-stu-id="92509-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="92509-110">例子</span><span class="sxs-lookup"><span data-stu-id="92509-110">EXAMPLES</span></span>

### <span data-ttu-id="92509-111">範例 1：取得 DSC 節點的所有報表</span><span class="sxs-lookup"><span data-stu-id="92509-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="92509-112">第一個命令會針對名為 Contoso17 的自動化帳戶名為 Computer14 的電腦，獲得 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="92509-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="92509-113">命令會在此變數中$Node物件。</span><span class="sxs-lookup"><span data-stu-id="92509-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="92509-114">第二個命令會針對從名為 Computer14 的 DSC 節點到 Contoso17 自動化帳戶的所有報表，獲得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="92509-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="92509-115">命令會使用物件的 **Id** 屬性指定$Node。</span><span class="sxs-lookup"><span data-stu-id="92509-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="92509-116">範例 2：根據報表識別碼取得 DSC 節點的報表</span><span class="sxs-lookup"><span data-stu-id="92509-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="92509-117">第一個命令會針對名為 Contoso17 的自動化帳戶名為 Computer14 的電腦，獲得 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="92509-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="92509-118">命令會在此變數中$Node物件。</span><span class="sxs-lookup"><span data-stu-id="92509-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="92509-119">第二個命令會針對從名為 Computer14 的 DSC 節點到名為 Contoso17 的自動化帳戶的指定識別碼所識別的報告，獲得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="92509-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="92509-120">範例 3：取得 DSC 節點的最新報表</span><span class="sxs-lookup"><span data-stu-id="92509-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="92509-121">第一個命令會針對名為 Contoso17 的自動化帳戶名為 Computer14 的電腦，獲得 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="92509-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="92509-122">命令會在此變數中$Node物件。</span><span class="sxs-lookup"><span data-stu-id="92509-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="92509-123">第二個命令會針對從名為 Computer14 的 DSC 節點到 Contoso17 自動化帳戶的最新報表，獲得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="92509-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="92509-124">參數</span><span class="sxs-lookup"><span data-stu-id="92509-124">PARAMETERS</span></span>

### <span data-ttu-id="92509-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="92509-125">-AutomationAccountName</span></span>
<span data-ttu-id="92509-126">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="92509-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="92509-127">此 Cmdlet 會針對屬於此參數指定之帳戶的 DSC 節點匯出報表。</span><span class="sxs-lookup"><span data-stu-id="92509-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="92509-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92509-128">-DefaultProfile</span></span>
<span data-ttu-id="92509-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="92509-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92509-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="92509-130">-EndTime</span></span>
<span data-ttu-id="92509-131">指定結束時間。</span><span class="sxs-lookup"><span data-stu-id="92509-131">Specifies an end time.</span></span>
<span data-ttu-id="92509-132">此 Cmdlet 會獲得自動化在此時之前收到的報告。</span><span class="sxs-lookup"><span data-stu-id="92509-132">This cmdlet gets reports that Automation received before this time.</span></span>

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

### <span data-ttu-id="92509-133">-Id</span><span class="sxs-lookup"><span data-stu-id="92509-133">-Id</span></span>
<span data-ttu-id="92509-134">指定此 Cmdlet 取得之 DSC 節點報表的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="92509-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

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

### <span data-ttu-id="92509-135">-最新</span><span class="sxs-lookup"><span data-stu-id="92509-135">-Latest</span></span>
<span data-ttu-id="92509-136">表示此 Cmdlet 只會為指定的節點獲得最新的 DSC 報表。</span><span class="sxs-lookup"><span data-stu-id="92509-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

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

### <span data-ttu-id="92509-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="92509-137">-NodeId</span></span>
<span data-ttu-id="92509-138">指定此 Cmdlet 會獲得報表之 DSC 節點的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="92509-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="92509-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92509-139">-ResourceGroupName</span></span>
<span data-ttu-id="92509-140">指定包含此 Cmdlet 會獲得報表之 DSC 節點的資源組名。</span><span class="sxs-lookup"><span data-stu-id="92509-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="92509-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="92509-141">-StartTime</span></span>
<span data-ttu-id="92509-142">指定開始時間。</span><span class="sxs-lookup"><span data-stu-id="92509-142">Specifies a start time.</span></span>
<span data-ttu-id="92509-143">此 Cmdlet 會獲得自動化在此時間之後收到的報告。</span><span class="sxs-lookup"><span data-stu-id="92509-143">This cmdlet gets reports that Automation received after this time.</span></span>

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

### <span data-ttu-id="92509-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92509-144">CommonParameters</span></span>
<span data-ttu-id="92509-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="92509-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92509-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="92509-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92509-147">輸入</span><span class="sxs-lookup"><span data-stu-id="92509-147">INPUTS</span></span>

### <span data-ttu-id="92509-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="92509-148">System.Guid</span></span>

### <span data-ttu-id="92509-149">System.Nullable'1[[System.DateTimeOffset， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="92509-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="92509-150">System.String</span><span class="sxs-lookup"><span data-stu-id="92509-150">System.String</span></span>

## <span data-ttu-id="92509-151">輸出</span><span class="sxs-lookup"><span data-stu-id="92509-151">OUTPUTS</span></span>

### <span data-ttu-id="92509-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="92509-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="92509-153">筆記</span><span class="sxs-lookup"><span data-stu-id="92509-153">NOTES</span></span>

## <span data-ttu-id="92509-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="92509-154">RELATED LINKS</span></span>

[<span data-ttu-id="92509-155">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="92509-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="92509-156">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="92509-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


