---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: 2d7c038f9f226f074bfe534df40471959607f3d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444056"
---
# <span data-ttu-id="539b5-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="539b5-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="539b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="539b5-102">SYNOPSIS</span></span>
<span data-ttu-id="539b5-103">建立自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="539b5-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="539b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="539b5-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="539b5-105">說明</span><span class="sxs-lookup"><span data-stu-id="539b5-105">DESCRIPTION</span></span>
<span data-ttu-id="539b5-106">**新的-AzureRmAutomationAccount** Cmdlet 會在資源群組中建立 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="539b5-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>
<span data-ttu-id="539b5-107">自動化帳戶是與其他自動化帳戶資源隔離的自動化資源容器。</span><span class="sxs-lookup"><span data-stu-id="539b5-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="539b5-108">自動化資源包括 runbook、所需的狀態設定 (DSC) 設定、作業和資產。</span><span class="sxs-lookup"><span data-stu-id="539b5-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="539b5-109">示例</span><span class="sxs-lookup"><span data-stu-id="539b5-109">EXAMPLES</span></span>

### <span data-ttu-id="539b5-110">範例1：建立自動化帳戶</span><span class="sxs-lookup"><span data-stu-id="539b5-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="539b5-111">這個命令會在東美國地區建立名為 ContosoAutomationAccount 的新自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="539b5-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="539b5-112">參數</span><span class="sxs-lookup"><span data-stu-id="539b5-112">PARAMETERS</span></span>

### <span data-ttu-id="539b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="539b5-113">-DefaultProfile</span></span>
<span data-ttu-id="539b5-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="539b5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="539b5-115">-位置</span><span class="sxs-lookup"><span data-stu-id="539b5-115">-Location</span></span>
<span data-ttu-id="539b5-116">指定此 Cmdlet 建立自動化帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="539b5-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="539b5-117">若要取得有效的位置，請使用 Get-AzureRMLocation Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="539b5-117">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="539b5-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="539b5-118">-Name</span></span>
<span data-ttu-id="539b5-119">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="539b5-119">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="539b5-120">-方案</span><span class="sxs-lookup"><span data-stu-id="539b5-120">-Plan</span></span>
<span data-ttu-id="539b5-121">指定自動化帳戶的方案。</span><span class="sxs-lookup"><span data-stu-id="539b5-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="539b5-122">有效值為：</span><span class="sxs-lookup"><span data-stu-id="539b5-122">Valid values are:</span></span>
- <span data-ttu-id="539b5-123">空白</span><span class="sxs-lookup"><span data-stu-id="539b5-123">Basic</span></span>
- <span data-ttu-id="539b5-124">空閒</span><span class="sxs-lookup"><span data-stu-id="539b5-124">Free</span></span>

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

### <span data-ttu-id="539b5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="539b5-125">-ResourceGroupName</span></span>
<span data-ttu-id="539b5-126">指定此 Cmdlet 新增自動化帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="539b5-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="539b5-127">-標記</span><span class="sxs-lookup"><span data-stu-id="539b5-127">-Tags</span></span>
<span data-ttu-id="539b5-128">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="539b5-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="539b5-129">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="539b5-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="539b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539b5-130">CommonParameters</span></span>
<span data-ttu-id="539b5-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="539b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539b5-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="539b5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539b5-133">輸入</span><span class="sxs-lookup"><span data-stu-id="539b5-133">INPUTS</span></span>

### <span data-ttu-id="539b5-134">System.object</span><span class="sxs-lookup"><span data-stu-id="539b5-134">System.String</span></span>

### <span data-ttu-id="539b5-135">System.object</span><span class="sxs-lookup"><span data-stu-id="539b5-135">System.Collections.IDictionary</span></span>

## <span data-ttu-id="539b5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="539b5-136">OUTPUTS</span></span>

### <span data-ttu-id="539b5-137">AutomationAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="539b5-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="539b5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="539b5-138">NOTES</span></span>

## <span data-ttu-id="539b5-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="539b5-139">RELATED LINKS</span></span>

[<span data-ttu-id="539b5-140">AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="539b5-140">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="539b5-141">移除-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="539b5-141">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="539b5-142">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="539b5-142">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
