---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
ms.openlocfilehash: 4486301d6a7e39081e297d018f3aa244459d328b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623021"
---
# <span data-ttu-id="12cd1-101">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="12cd1-101">New-AzAutomationAccount</span></span>

## <span data-ttu-id="12cd1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="12cd1-103">建立自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="12cd1-103">Creates an Automation account.</span></span>

## <span data-ttu-id="12cd1-104">句法</span><span class="sxs-lookup"><span data-stu-id="12cd1-104">SYNTAX</span></span>

```
New-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12cd1-105">說明</span><span class="sxs-lookup"><span data-stu-id="12cd1-105">DESCRIPTION</span></span>
<span data-ttu-id="12cd1-106">**新的-AzAutomationAccount** Cmdlet 會在資源群組中建立 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="12cd1-106">The **New-AzAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>
<span data-ttu-id="12cd1-107">自動化帳戶是與其他自動化帳戶資源隔離的自動化資源容器。</span><span class="sxs-lookup"><span data-stu-id="12cd1-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="12cd1-108">自動化資源包括 runbook、所需的狀態設定 (DSC) 設定、作業和資產。</span><span class="sxs-lookup"><span data-stu-id="12cd1-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="12cd1-109">示例</span><span class="sxs-lookup"><span data-stu-id="12cd1-109">EXAMPLES</span></span>

### <span data-ttu-id="12cd1-110">範例1：建立自動化帳戶</span><span class="sxs-lookup"><span data-stu-id="12cd1-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="12cd1-111">這個命令會在東美國地區建立名為 ContosoAutomationAccount 的新自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="12cd1-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="12cd1-112">參數</span><span class="sxs-lookup"><span data-stu-id="12cd1-112">PARAMETERS</span></span>

### <span data-ttu-id="12cd1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12cd1-113">-DefaultProfile</span></span>
<span data-ttu-id="12cd1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="12cd1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12cd1-115">-位置</span><span class="sxs-lookup"><span data-stu-id="12cd1-115">-Location</span></span>
<span data-ttu-id="12cd1-116">指定此 Cmdlet 建立自動化帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="12cd1-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="12cd1-117">若要取得有效的位置，請使用 Get-AzLocation Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12cd1-117">To obtain valid locations, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="12cd1-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="12cd1-118">-Name</span></span>
<span data-ttu-id="12cd1-119">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="12cd1-119">Specifies a name for the Automation account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12cd1-120">-方案</span><span class="sxs-lookup"><span data-stu-id="12cd1-120">-Plan</span></span>
<span data-ttu-id="12cd1-121">指定自動化帳戶的方案。</span><span class="sxs-lookup"><span data-stu-id="12cd1-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="12cd1-122">有效值為：</span><span class="sxs-lookup"><span data-stu-id="12cd1-122">Valid values are:</span></span>
- <span data-ttu-id="12cd1-123">空白</span><span class="sxs-lookup"><span data-stu-id="12cd1-123">Basic</span></span>
- <span data-ttu-id="12cd1-124">空閒</span><span class="sxs-lookup"><span data-stu-id="12cd1-124">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12cd1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12cd1-125">-ResourceGroupName</span></span>
<span data-ttu-id="12cd1-126">指定此 Cmdlet 新增自動化帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="12cd1-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="12cd1-127">-標記</span><span class="sxs-lookup"><span data-stu-id="12cd1-127">-Tags</span></span>
<span data-ttu-id="12cd1-128">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="12cd1-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="12cd1-129">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="12cd1-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12cd1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12cd1-130">CommonParameters</span></span>
<span data-ttu-id="12cd1-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12cd1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12cd1-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12cd1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12cd1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="12cd1-133">INPUTS</span></span>

### <span data-ttu-id="12cd1-134">System.object</span><span class="sxs-lookup"><span data-stu-id="12cd1-134">System.String</span></span>

### <span data-ttu-id="12cd1-135">System.object</span><span class="sxs-lookup"><span data-stu-id="12cd1-135">System.Collections.IDictionary</span></span>

## <span data-ttu-id="12cd1-136">輸出</span><span class="sxs-lookup"><span data-stu-id="12cd1-136">OUTPUTS</span></span>

### <span data-ttu-id="12cd1-137">AutomationAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="12cd1-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="12cd1-138">筆記</span><span class="sxs-lookup"><span data-stu-id="12cd1-138">NOTES</span></span>

## <span data-ttu-id="12cd1-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="12cd1-139">RELATED LINKS</span></span>

[<span data-ttu-id="12cd1-140">AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="12cd1-140">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="12cd1-141">移除-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="12cd1-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="12cd1-142">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="12cd1-142">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)
