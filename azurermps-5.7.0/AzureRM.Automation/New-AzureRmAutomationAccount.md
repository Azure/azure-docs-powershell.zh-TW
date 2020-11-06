---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: c82a68e7859945b1fdb91f6d44a1ebbcef6d2cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446556"
---
# <span data-ttu-id="64ed0-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="64ed0-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="64ed0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="64ed0-103">建立自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="64ed0-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64ed0-104">句法</span><span class="sxs-lookup"><span data-stu-id="64ed0-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64ed0-105">說明</span><span class="sxs-lookup"><span data-stu-id="64ed0-105">DESCRIPTION</span></span>
<span data-ttu-id="64ed0-106">**新的-AzureRmAutomationAccount** Cmdlet 會在資源群組中建立 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="64ed0-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="64ed0-107">自動化帳戶是與其他自動化帳戶資源隔離的自動化資源容器。</span><span class="sxs-lookup"><span data-stu-id="64ed0-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="64ed0-108">自動化資源包括 runbook、所需的狀態設定 (DSC) 設定、作業和資產。</span><span class="sxs-lookup"><span data-stu-id="64ed0-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="64ed0-109">示例</span><span class="sxs-lookup"><span data-stu-id="64ed0-109">EXAMPLES</span></span>

### <span data-ttu-id="64ed0-110">範例1：建立自動化帳戶</span><span class="sxs-lookup"><span data-stu-id="64ed0-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="64ed0-111">這個命令會在東美國地區建立名為 ContosoAutomationAccount 的新自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="64ed0-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="64ed0-112">參數</span><span class="sxs-lookup"><span data-stu-id="64ed0-112">PARAMETERS</span></span>

### <span data-ttu-id="64ed0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ed0-113">-DefaultProfile</span></span>
<span data-ttu-id="64ed0-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="64ed0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64ed0-115">-位置</span><span class="sxs-lookup"><span data-stu-id="64ed0-115">-Location</span></span>
<span data-ttu-id="64ed0-116">指定此 Cmdlet 建立自動化帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="64ed0-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="64ed0-117">若要取得有效的位置，請使用 Get-AzureRMLocation Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64ed0-117">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64ed0-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="64ed0-118">-Name</span></span>
<span data-ttu-id="64ed0-119">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ed0-119">Specifies a name for the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64ed0-120">-方案</span><span class="sxs-lookup"><span data-stu-id="64ed0-120">-Plan</span></span>
<span data-ttu-id="64ed0-121">指定自動化帳戶的方案。</span><span class="sxs-lookup"><span data-stu-id="64ed0-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="64ed0-122">有效值為：</span><span class="sxs-lookup"><span data-stu-id="64ed0-122">Valid values are:</span></span>

- <span data-ttu-id="64ed0-123">空白</span><span class="sxs-lookup"><span data-stu-id="64ed0-123">Basic</span></span>
- <span data-ttu-id="64ed0-124">空閒</span><span class="sxs-lookup"><span data-stu-id="64ed0-124">Free</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64ed0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64ed0-125">-ResourceGroupName</span></span>
<span data-ttu-id="64ed0-126">指定此 Cmdlet 新增自動化帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ed0-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="64ed0-127">-標記</span><span class="sxs-lookup"><span data-stu-id="64ed0-127">-Tags</span></span>
<span data-ttu-id="64ed0-128">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="64ed0-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="64ed0-129">例如：</span><span class="sxs-lookup"><span data-stu-id="64ed0-129">For example:</span></span>

<span data-ttu-id="64ed0-130">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="64ed0-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64ed0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ed0-131">CommonParameters</span></span>
<span data-ttu-id="64ed0-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64ed0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ed0-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="64ed0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ed0-134">輸入</span><span class="sxs-lookup"><span data-stu-id="64ed0-134">INPUTS</span></span>

### <span data-ttu-id="64ed0-135">所有</span><span class="sxs-lookup"><span data-stu-id="64ed0-135">None</span></span>
<span data-ttu-id="64ed0-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="64ed0-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64ed0-137">輸出</span><span class="sxs-lookup"><span data-stu-id="64ed0-137">OUTPUTS</span></span>

### <span data-ttu-id="64ed0-138">AutomationAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="64ed0-138">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="64ed0-139">筆記</span><span class="sxs-lookup"><span data-stu-id="64ed0-139">NOTES</span></span>

## <span data-ttu-id="64ed0-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="64ed0-140">RELATED LINKS</span></span>

[<span data-ttu-id="64ed0-141">AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="64ed0-141">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="64ed0-142">移除-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="64ed0-142">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="64ed0-143">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="64ed0-143">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
