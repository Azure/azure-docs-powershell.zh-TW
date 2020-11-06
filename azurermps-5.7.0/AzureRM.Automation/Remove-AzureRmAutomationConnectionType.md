---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
ms.openlocfilehash: c76475a36536e6da68bc7ec5a39790ee96409ea3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444776"
---
# <span data-ttu-id="9a5b0-101">Remove-AzureRmAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="9a5b0-101">Remove-AzureRmAutomationConnectionType</span></span>

## <span data-ttu-id="9a5b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5b0-103">移除自動化連線類型。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-103">Removes an Automation connection type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a5b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a5b0-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a5b0-105">說明</span><span class="sxs-lookup"><span data-stu-id="9a5b0-105">DESCRIPTION</span></span>
<span data-ttu-id="9a5b0-106">**AzureRmAutomationConnectionType** Cmdlet 會從 Azure 自動化中移除連線類型。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-106">The **Remove-AzureRmAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>

<span data-ttu-id="9a5b0-107">所有與您刪除之連線類型相關聯的連線都無法使用。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="9a5b0-108">除非您建立符合下列條件的新連線類型，否則請移除它們：</span><span class="sxs-lookup"><span data-stu-id="9a5b0-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 

- <span data-ttu-id="9a5b0-109">類型與原始連線類型的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="9a5b0-110">該類型具有與原始連線類型相同的欄位定義。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="9a5b0-111">它可以有其他欄位。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-111">It can have additional fields.</span></span>

## <span data-ttu-id="9a5b0-112">示例</span><span class="sxs-lookup"><span data-stu-id="9a5b0-112">EXAMPLES</span></span>

### <span data-ttu-id="9a5b0-113">範例1：移除連線類型</span><span class="sxs-lookup"><span data-stu-id="9a5b0-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzureRmAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9a5b0-114">這個命令會在名為 Contoso17 的自動化帳戶中，移除一個名為 ContosoConnectionType 的連線類型。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9a5b0-115">參數</span><span class="sxs-lookup"><span data-stu-id="9a5b0-115">PARAMETERS</span></span>

### <span data-ttu-id="9a5b0-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9a5b0-116">-AutomationAccountName</span></span>
<span data-ttu-id="9a5b0-117">指定此 Cmdlet 移除連線類型之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a5b0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a5b0-118">-DefaultProfile</span></span>
<span data-ttu-id="9a5b0-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9a5b0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a5b0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9a5b0-120">-Force</span></span>
<span data-ttu-id="9a5b0-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="9a5b0-121">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5b0-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9a5b0-122">-Name</span></span>
<span data-ttu-id="9a5b0-123">指定此 Cmdlet 移除之自動化連線類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9a5b0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a5b0-124">-ResourceGroupName</span></span>
<span data-ttu-id="9a5b0-125">指定此 Cmdlet 移除自動化連線類型之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="9a5b0-126">-確認</span><span class="sxs-lookup"><span data-stu-id="9a5b0-126">-Confirm</span></span>
<span data-ttu-id="9a5b0-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5b0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a5b0-128">-WhatIf</span></span>
<span data-ttu-id="9a5b0-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a5b0-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5b0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5b0-131">CommonParameters</span></span>
<span data-ttu-id="9a5b0-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5b0-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5b0-134">輸入</span><span class="sxs-lookup"><span data-stu-id="9a5b0-134">INPUTS</span></span>

### <span data-ttu-id="9a5b0-135">所有</span><span class="sxs-lookup"><span data-stu-id="9a5b0-135">None</span></span>
<span data-ttu-id="9a5b0-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9a5b0-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9a5b0-137">輸出</span><span class="sxs-lookup"><span data-stu-id="9a5b0-137">OUTPUTS</span></span>

## <span data-ttu-id="9a5b0-138">筆記</span><span class="sxs-lookup"><span data-stu-id="9a5b0-138">NOTES</span></span>

## <span data-ttu-id="9a5b0-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a5b0-139">RELATED LINKS</span></span>

[<span data-ttu-id="9a5b0-140">移除-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9a5b0-140">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


