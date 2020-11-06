---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
ms.openlocfilehash: 4fb4bbab5c774cacd274754a106aacfeebdb533c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456248"
---
# <span data-ttu-id="a8e60-101">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a8e60-101">Remove-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="a8e60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8e60-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e60-103">移除 [自動化] 連線。</span><span class="sxs-lookup"><span data-stu-id="a8e60-103">Removes an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8e60-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8e60-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8e60-105">說明</span><span class="sxs-lookup"><span data-stu-id="a8e60-105">DESCRIPTION</span></span>
<span data-ttu-id="a8e60-106">**AzureRmAutomationConnection** Cmdlet 會從 Azure 自動化中移除連線。</span><span class="sxs-lookup"><span data-stu-id="a8e60-106">The **Remove-AzureRmAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="a8e60-107">示例</span><span class="sxs-lookup"><span data-stu-id="a8e60-107">EXAMPLES</span></span>

### <span data-ttu-id="a8e60-108">範例1：移除連線</span><span class="sxs-lookup"><span data-stu-id="a8e60-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzureRmAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a8e60-109">這個命令會在名為 [Contoso17] 的自動化帳戶中移除名為 ContosoConnection 的憑證。</span><span class="sxs-lookup"><span data-stu-id="a8e60-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a8e60-110">參數</span><span class="sxs-lookup"><span data-stu-id="a8e60-110">PARAMETERS</span></span>

### <span data-ttu-id="a8e60-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a8e60-111">-AutomationAccountName</span></span>
<span data-ttu-id="a8e60-112">指定此 Cmdlet 移除連線之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8e60-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="a8e60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8e60-113">-DefaultProfile</span></span>
<span data-ttu-id="a8e60-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a8e60-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8e60-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a8e60-115">-Force</span></span>
<span data-ttu-id="a8e60-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="a8e60-116">ps_force</span></span>

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

### <span data-ttu-id="a8e60-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8e60-117">-Name</span></span>
<span data-ttu-id="a8e60-118">指定此 Cmdlet 移除的連線名稱。</span><span class="sxs-lookup"><span data-stu-id="a8e60-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a8e60-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8e60-119">-ResourceGroupName</span></span>
<span data-ttu-id="a8e60-120">指定此 Cmdlet 移除連線之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8e60-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="a8e60-121">-確認</span><span class="sxs-lookup"><span data-stu-id="a8e60-121">-Confirm</span></span>
<span data-ttu-id="a8e60-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a8e60-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8e60-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8e60-123">-WhatIf</span></span>
<span data-ttu-id="a8e60-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8e60-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8e60-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8e60-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8e60-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e60-126">CommonParameters</span></span>
<span data-ttu-id="a8e60-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8e60-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e60-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a8e60-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e60-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a8e60-129">INPUTS</span></span>

### <span data-ttu-id="a8e60-130">所有</span><span class="sxs-lookup"><span data-stu-id="a8e60-130">None</span></span>
<span data-ttu-id="a8e60-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a8e60-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8e60-132">輸出</span><span class="sxs-lookup"><span data-stu-id="a8e60-132">OUTPUTS</span></span>

## <span data-ttu-id="a8e60-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a8e60-133">NOTES</span></span>

## <span data-ttu-id="a8e60-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8e60-134">RELATED LINKS</span></span>

[<span data-ttu-id="a8e60-135">AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a8e60-135">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="a8e60-136">新-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a8e60-136">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


