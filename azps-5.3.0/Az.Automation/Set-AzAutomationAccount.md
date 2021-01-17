---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: f32e9c0d76e88fba5475abb39595b0a6c4bea834
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447135"
---
# <span data-ttu-id="336fb-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="336fb-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="336fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="336fb-102">SYNOPSIS</span></span>
<span data-ttu-id="336fb-103">修改自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="336fb-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="336fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="336fb-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="336fb-105">說明</span><span class="sxs-lookup"><span data-stu-id="336fb-105">DESCRIPTION</span></span>
<span data-ttu-id="336fb-106">**AzAutomationAccount** Cmdlet 會修改 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="336fb-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="336fb-107">如需自動化帳戶的詳細資訊，請參閱 New-AzAutomationAccount Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="336fb-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="336fb-108">示例</span><span class="sxs-lookup"><span data-stu-id="336fb-108">EXAMPLES</span></span>

### <span data-ttu-id="336fb-109">範例1：設定自動化帳戶的標記</span><span class="sxs-lookup"><span data-stu-id="336fb-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="336fb-110">第一個命令會將兩個鍵/值對指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="336fb-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="336fb-111">第二個命令會在 $Tags 中為名為 AutomationAccount01 的自動化帳戶設定標記。</span><span class="sxs-lookup"><span data-stu-id="336fb-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="336fb-112">範例2：變更自動化帳戶的方案</span><span class="sxs-lookup"><span data-stu-id="336fb-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="336fb-113">這個命令會將計畫變更為基本的自動化帳戶（名為 AutomationAccount01）。</span><span class="sxs-lookup"><span data-stu-id="336fb-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="336fb-114">參數</span><span class="sxs-lookup"><span data-stu-id="336fb-114">PARAMETERS</span></span>

### <span data-ttu-id="336fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="336fb-115">-DefaultProfile</span></span>
<span data-ttu-id="336fb-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="336fb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="336fb-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="336fb-117">-Name</span></span>
<span data-ttu-id="336fb-118">指定此 Cmdlet 所修改之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="336fb-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="336fb-119">-方案</span><span class="sxs-lookup"><span data-stu-id="336fb-119">-Plan</span></span>
<span data-ttu-id="336fb-120">指定自動化帳戶的方案。</span><span class="sxs-lookup"><span data-stu-id="336fb-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="336fb-121">有效值為：</span><span class="sxs-lookup"><span data-stu-id="336fb-121">Valid values are:</span></span>
- <span data-ttu-id="336fb-122">空白</span><span class="sxs-lookup"><span data-stu-id="336fb-122">Basic</span></span>
- <span data-ttu-id="336fb-123">空閒</span><span class="sxs-lookup"><span data-stu-id="336fb-123">Free</span></span>

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

### <span data-ttu-id="336fb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="336fb-124">-ResourceGroupName</span></span>
<span data-ttu-id="336fb-125">指定包含此 Cmdlet 所修改之自動化帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="336fb-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="336fb-126">-標記</span><span class="sxs-lookup"><span data-stu-id="336fb-126">-Tags</span></span>
<span data-ttu-id="336fb-127">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="336fb-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="336fb-128">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="336fb-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="336fb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336fb-129">CommonParameters</span></span>
<span data-ttu-id="336fb-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="336fb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336fb-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="336fb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336fb-132">輸入</span><span class="sxs-lookup"><span data-stu-id="336fb-132">INPUTS</span></span>

### <span data-ttu-id="336fb-133">System.object</span><span class="sxs-lookup"><span data-stu-id="336fb-133">System.String</span></span>

### <span data-ttu-id="336fb-134">System.object</span><span class="sxs-lookup"><span data-stu-id="336fb-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="336fb-135">輸出</span><span class="sxs-lookup"><span data-stu-id="336fb-135">OUTPUTS</span></span>

### <span data-ttu-id="336fb-136">AutomationAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="336fb-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="336fb-137">筆記</span><span class="sxs-lookup"><span data-stu-id="336fb-137">NOTES</span></span>

## <span data-ttu-id="336fb-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="336fb-138">RELATED LINKS</span></span>

[<span data-ttu-id="336fb-139">AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="336fb-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="336fb-140">新-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="336fb-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="336fb-141">移除-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="336fb-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
