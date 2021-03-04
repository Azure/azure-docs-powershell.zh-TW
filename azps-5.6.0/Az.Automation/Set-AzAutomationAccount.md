---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: bc810da3cd43a18506160d03e6c172eb272bd797
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916655"
---
# <span data-ttu-id="7386a-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7386a-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="7386a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7386a-102">SYNOPSIS</span></span>
<span data-ttu-id="7386a-103">修改自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="7386a-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="7386a-104">語法</span><span class="sxs-lookup"><span data-stu-id="7386a-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7386a-105">描述</span><span class="sxs-lookup"><span data-stu-id="7386a-105">DESCRIPTION</span></span>
<span data-ttu-id="7386a-106">**Set-AzAutomationAccount** Cmdlet 會修改 Azure Automation 帳戶。</span><span class="sxs-lookup"><span data-stu-id="7386a-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="7386a-107">有關自動化帳戶的資訊，請參閱 New-AzAutomationAccount Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7386a-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="7386a-108">例子</span><span class="sxs-lookup"><span data-stu-id="7386a-108">EXAMPLES</span></span>

### <span data-ttu-id="7386a-109">範例 1：設定自動化帳戶的標記</span><span class="sxs-lookup"><span data-stu-id="7386a-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="7386a-110">第一個命令會指派兩組按鍵/值組給$Tags變數。</span><span class="sxs-lookup"><span data-stu-id="7386a-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="7386a-111">第二個命令會為自動化$Tags AutomationAccount01 設定標記。</span><span class="sxs-lookup"><span data-stu-id="7386a-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="7386a-112">範例 2：變更自動化帳戶的計畫</span><span class="sxs-lookup"><span data-stu-id="7386a-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="7386a-113">此命令將自動化帳戶的 Plan 變更為 Basic，名為 AutomationAccount01。</span><span class="sxs-lookup"><span data-stu-id="7386a-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="7386a-114">參數</span><span class="sxs-lookup"><span data-stu-id="7386a-114">PARAMETERS</span></span>

### <span data-ttu-id="7386a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7386a-115">-DefaultProfile</span></span>
<span data-ttu-id="7386a-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7386a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7386a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="7386a-117">-Name</span></span>
<span data-ttu-id="7386a-118">指定此 Cmdlet 修改的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7386a-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7386a-119">-規劃</span><span class="sxs-lookup"><span data-stu-id="7386a-119">-Plan</span></span>
<span data-ttu-id="7386a-120">指定自動化帳戶的計畫。</span><span class="sxs-lookup"><span data-stu-id="7386a-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="7386a-121">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="7386a-121">Valid values are:</span></span>
- <span data-ttu-id="7386a-122">基本</span><span class="sxs-lookup"><span data-stu-id="7386a-122">Basic</span></span>
- <span data-ttu-id="7386a-123">自由</span><span class="sxs-lookup"><span data-stu-id="7386a-123">Free</span></span>

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

### <span data-ttu-id="7386a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7386a-124">-ResourceGroupName</span></span>
<span data-ttu-id="7386a-125">指定包含此 Cmdlet 修改之自動化帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7386a-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7386a-126">-標記</span><span class="sxs-lookup"><span data-stu-id="7386a-126">-Tags</span></span>
<span data-ttu-id="7386a-127">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="7386a-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7386a-128">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="7386a-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7386a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7386a-129">CommonParameters</span></span>
<span data-ttu-id="7386a-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7386a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7386a-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7386a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7386a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7386a-132">INPUTS</span></span>

### <span data-ttu-id="7386a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7386a-133">System.String</span></span>

### <span data-ttu-id="7386a-134">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="7386a-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="7386a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7386a-135">OUTPUTS</span></span>

### <span data-ttu-id="7386a-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7386a-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="7386a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7386a-137">NOTES</span></span>

## <span data-ttu-id="7386a-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7386a-138">RELATED LINKS</span></span>

[<span data-ttu-id="7386a-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7386a-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="7386a-140">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7386a-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="7386a-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7386a-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
