---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: 7a0341221dee0f282508377d1233e30deae1fcee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623434"
---
# <span data-ttu-id="7c607-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7c607-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="7c607-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c607-102">SYNOPSIS</span></span>
<span data-ttu-id="7c607-103">修改自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="7c607-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c607-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c607-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c607-105">說明</span><span class="sxs-lookup"><span data-stu-id="7c607-105">DESCRIPTION</span></span>
<span data-ttu-id="7c607-106">**AzureRmAutomationAccount** Cmdlet 會修改 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="7c607-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="7c607-107">如需自動化帳戶的詳細資訊，請參閱 New-AzureRmAutomationAccount Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c607-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="7c607-108">示例</span><span class="sxs-lookup"><span data-stu-id="7c607-108">EXAMPLES</span></span>

### <span data-ttu-id="7c607-109">範例1：設定自動化帳戶的標記</span><span class="sxs-lookup"><span data-stu-id="7c607-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="7c607-110">第一個命令會將兩個鍵/值對指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="7c607-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="7c607-111">第二個命令會在 $Tags 中為名為 AutomationAccount01 的自動化帳戶設定標記。</span><span class="sxs-lookup"><span data-stu-id="7c607-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="7c607-112">範例2：變更自動化帳戶的方案</span><span class="sxs-lookup"><span data-stu-id="7c607-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="7c607-113">這個命令會將計畫變更為基本的自動化帳戶（名為 AutomationAccount01）。</span><span class="sxs-lookup"><span data-stu-id="7c607-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="7c607-114">參數</span><span class="sxs-lookup"><span data-stu-id="7c607-114">PARAMETERS</span></span>

### <span data-ttu-id="7c607-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c607-115">-DefaultProfile</span></span>
<span data-ttu-id="7c607-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7c607-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c607-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c607-117">-Name</span></span>
<span data-ttu-id="7c607-118">指定此 Cmdlet 所修改之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c607-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7c607-119">-方案</span><span class="sxs-lookup"><span data-stu-id="7c607-119">-Plan</span></span>
<span data-ttu-id="7c607-120">指定自動化帳戶的方案。</span><span class="sxs-lookup"><span data-stu-id="7c607-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="7c607-121">有效值為：</span><span class="sxs-lookup"><span data-stu-id="7c607-121">Valid values are:</span></span>
- <span data-ttu-id="7c607-122">空白</span><span class="sxs-lookup"><span data-stu-id="7c607-122">Basic</span></span>
- <span data-ttu-id="7c607-123">空閒</span><span class="sxs-lookup"><span data-stu-id="7c607-123">Free</span></span>

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

### <span data-ttu-id="7c607-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c607-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c607-125">指定包含此 Cmdlet 所修改之自動化帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c607-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7c607-126">-標記</span><span class="sxs-lookup"><span data-stu-id="7c607-126">-Tags</span></span>
<span data-ttu-id="7c607-127">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="7c607-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7c607-128">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7c607-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7c607-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c607-129">CommonParameters</span></span>
<span data-ttu-id="7c607-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c607-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c607-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c607-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c607-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7c607-132">INPUTS</span></span>

### <span data-ttu-id="7c607-133">System.object</span><span class="sxs-lookup"><span data-stu-id="7c607-133">System.String</span></span>

### <span data-ttu-id="7c607-134">System.object</span><span class="sxs-lookup"><span data-stu-id="7c607-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="7c607-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7c607-135">OUTPUTS</span></span>

### <span data-ttu-id="7c607-136">AutomationAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7c607-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="7c607-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7c607-137">NOTES</span></span>

## <span data-ttu-id="7c607-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c607-138">RELATED LINKS</span></span>

[<span data-ttu-id="7c607-139">AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7c607-139">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="7c607-140">新-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7c607-140">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="7c607-141">移除-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7c607-141">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)
