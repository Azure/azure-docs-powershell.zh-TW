---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 2c98cde73610a7a72b237bbe268f527fefaf71a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450888"
---
# <span data-ttu-id="d27e8-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d27e8-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="d27e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d27e8-102">SYNOPSIS</span></span>
<span data-ttu-id="d27e8-103">移除自動化認證。</span><span class="sxs-lookup"><span data-stu-id="d27e8-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d27e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="d27e8-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d27e8-105">說明</span><span class="sxs-lookup"><span data-stu-id="d27e8-105">DESCRIPTION</span></span>
<span data-ttu-id="d27e8-106">**AzureRmAutomationCredential** Cmdlet 會從 Azure 自動化中移除認證。</span><span class="sxs-lookup"><span data-stu-id="d27e8-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="d27e8-107">示例</span><span class="sxs-lookup"><span data-stu-id="d27e8-107">EXAMPLES</span></span>

### <span data-ttu-id="d27e8-108">範例1：移除認證</span><span class="sxs-lookup"><span data-stu-id="d27e8-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d27e8-109">這個命令會在 Azure 自動化帳戶（名為 Contoso17）中移除一個名為 ContosoCredential 的認證。</span><span class="sxs-lookup"><span data-stu-id="d27e8-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d27e8-110">參數</span><span class="sxs-lookup"><span data-stu-id="d27e8-110">PARAMETERS</span></span>

### <span data-ttu-id="d27e8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d27e8-111">-AutomationAccountName</span></span>
<span data-ttu-id="d27e8-112">指定此 Cmdlet 移除認證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d27e8-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="d27e8-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="d27e8-113">-Name</span></span>
<span data-ttu-id="d27e8-114">指定此 Cmdlet 移除之認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="d27e8-114">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d27e8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d27e8-115">-ResourceGroupName</span></span>
<span data-ttu-id="d27e8-116">指定此 Cmdlet 移除認證之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d27e8-116">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="d27e8-117">-確認</span><span class="sxs-lookup"><span data-stu-id="d27e8-117">-Confirm</span></span>
<span data-ttu-id="d27e8-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d27e8-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d27e8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d27e8-119">-WhatIf</span></span>
<span data-ttu-id="d27e8-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d27e8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d27e8-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d27e8-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d27e8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d27e8-122">-DefaultProfile</span></span>
<span data-ttu-id="d27e8-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d27e8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d27e8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d27e8-124">CommonParameters</span></span>
<span data-ttu-id="d27e8-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d27e8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d27e8-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d27e8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d27e8-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d27e8-127">INPUTS</span></span>

## <span data-ttu-id="d27e8-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d27e8-128">OUTPUTS</span></span>

## <span data-ttu-id="d27e8-129">筆記</span><span class="sxs-lookup"><span data-stu-id="d27e8-129">NOTES</span></span>

## <span data-ttu-id="d27e8-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="d27e8-130">RELATED LINKS</span></span>

[<span data-ttu-id="d27e8-131">AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d27e8-131">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="d27e8-132">新-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d27e8-132">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="d27e8-133">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d27e8-133">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


