---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: 8ad63c37c366c0f9c7693585f3a3c2fd57de4fdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447180"
---
# <span data-ttu-id="e6c2e-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e6c2e-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="e6c2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c2e-103">修改自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="e6c2e-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6c2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6c2e-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6c2e-105">說明</span><span class="sxs-lookup"><span data-stu-id="e6c2e-105">DESCRIPTION</span></span>
<span data-ttu-id="e6c2e-106">**AzureRmAutomationAccount** Cmdlet 會修改 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="e6c2e-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>

<span data-ttu-id="e6c2e-107">如需自動化帳戶的詳細資訊，請參閱 New-AzureRmAutomationAccount Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6c2e-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="e6c2e-108">示例</span><span class="sxs-lookup"><span data-stu-id="e6c2e-108">EXAMPLES</span></span>

### <span data-ttu-id="e6c2e-109">範例1：設定自動化帳戶的標記</span><span class="sxs-lookup"><span data-stu-id="e6c2e-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="e6c2e-110">第一個命令會將兩個鍵/值對指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="e6c2e-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="e6c2e-111">第二個命令會在 $Tags 中為名為 AutomationAccount01 的自動化帳戶設定標記。</span><span class="sxs-lookup"><span data-stu-id="e6c2e-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="e6c2e-112">範例2：變更自動化帳戶的方案</span><span class="sxs-lookup"><span data-stu-id="e6c2e-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="e6c2e-113">這個命令會將計畫變更為基本的自動化帳戶（名為 AutomationAccount01）。</span><span class="sxs-lookup"><span data-stu-id="e6c2e-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="e6c2e-114">參數</span><span class="sxs-lookup"><span data-stu-id="e6c2e-114">PARAMETERS</span></span>

### <span data-ttu-id="e6c2e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6c2e-115">-Name</span></span>
<span data-ttu-id="e6c2e-116">指定此 Cmdlet 所修改之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6c2e-116">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e6c2e-117">-方案</span><span class="sxs-lookup"><span data-stu-id="e6c2e-117">-Plan</span></span>
<span data-ttu-id="e6c2e-118">指定自動化帳戶的方案。</span><span class="sxs-lookup"><span data-stu-id="e6c2e-118">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="e6c2e-119">有效值為：</span><span class="sxs-lookup"><span data-stu-id="e6c2e-119">Valid values are:</span></span>

- <span data-ttu-id="e6c2e-120">空白</span><span class="sxs-lookup"><span data-stu-id="e6c2e-120">Basic</span></span>
- <span data-ttu-id="e6c2e-121">空閒</span><span class="sxs-lookup"><span data-stu-id="e6c2e-121">Free</span></span>

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

### <span data-ttu-id="e6c2e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6c2e-122">-ResourceGroupName</span></span>
<span data-ttu-id="e6c2e-123">指定包含此 Cmdlet 所修改之自動化帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6c2e-123">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e6c2e-124">-標記</span><span class="sxs-lookup"><span data-stu-id="e6c2e-124">-Tags</span></span>
<span data-ttu-id="e6c2e-125">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="e6c2e-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e6c2e-126">例如：</span><span class="sxs-lookup"><span data-stu-id="e6c2e-126">For example:</span></span>

<span data-ttu-id="e6c2e-127">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e6c2e-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e6c2e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6c2e-128">-DefaultProfile</span></span>
<span data-ttu-id="e6c2e-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6c2e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6c2e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c2e-130">CommonParameters</span></span>
<span data-ttu-id="e6c2e-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6c2e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c2e-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e6c2e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c2e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e6c2e-133">INPUTS</span></span>

## <span data-ttu-id="e6c2e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e6c2e-134">OUTPUTS</span></span>

### <span data-ttu-id="e6c2e-135">AutomationAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e6c2e-135">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="e6c2e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e6c2e-136">NOTES</span></span>

## <span data-ttu-id="e6c2e-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6c2e-137">RELATED LINKS</span></span>

[<span data-ttu-id="e6c2e-138">AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e6c2e-138">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="e6c2e-139">新-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e6c2e-139">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="e6c2e-140">移除-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e6c2e-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)
