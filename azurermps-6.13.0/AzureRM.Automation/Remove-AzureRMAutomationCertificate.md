---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: 7498310c232fd623b131bdf9ae59136d9a4c500a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450319"
---
# <span data-ttu-id="64a27-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="64a27-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="64a27-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64a27-102">SYNOPSIS</span></span>
<span data-ttu-id="64a27-103">移除自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="64a27-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64a27-104">句法</span><span class="sxs-lookup"><span data-stu-id="64a27-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64a27-105">說明</span><span class="sxs-lookup"><span data-stu-id="64a27-105">DESCRIPTION</span></span>
<span data-ttu-id="64a27-106">**AzureRmAutomationCertificate** Cmdlet 會從 Azure 自動化中移除證書。</span><span class="sxs-lookup"><span data-stu-id="64a27-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="64a27-107">示例</span><span class="sxs-lookup"><span data-stu-id="64a27-107">EXAMPLES</span></span>

### <span data-ttu-id="64a27-108">範例1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="64a27-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="64a27-109">這個命令會在名為 [Contoso17] 的自動化帳戶中移除名為 Cert01 的憑證。</span><span class="sxs-lookup"><span data-stu-id="64a27-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="64a27-110">參數</span><span class="sxs-lookup"><span data-stu-id="64a27-110">PARAMETERS</span></span>

### <span data-ttu-id="64a27-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="64a27-111">-AutomationAccountName</span></span>
<span data-ttu-id="64a27-112">指定此 Cmdlet 移除憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="64a27-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="64a27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a27-113">-DefaultProfile</span></span>
<span data-ttu-id="64a27-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="64a27-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64a27-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="64a27-115">-Name</span></span>
<span data-ttu-id="64a27-116">指定此 Cmdlet 移除之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="64a27-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="64a27-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a27-117">-ResourceGroupName</span></span>
<span data-ttu-id="64a27-118">指定此 Cmdlet 移除憑證的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="64a27-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="64a27-119">-確認</span><span class="sxs-lookup"><span data-stu-id="64a27-119">-Confirm</span></span>
<span data-ttu-id="64a27-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="64a27-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64a27-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64a27-121">-WhatIf</span></span>
<span data-ttu-id="64a27-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64a27-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64a27-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64a27-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64a27-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a27-124">CommonParameters</span></span>
<span data-ttu-id="64a27-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64a27-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a27-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="64a27-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a27-127">輸入</span><span class="sxs-lookup"><span data-stu-id="64a27-127">INPUTS</span></span>

### <span data-ttu-id="64a27-128">System.object</span><span class="sxs-lookup"><span data-stu-id="64a27-128">System.String</span></span>

## <span data-ttu-id="64a27-129">輸出</span><span class="sxs-lookup"><span data-stu-id="64a27-129">OUTPUTS</span></span>

### <span data-ttu-id="64a27-130">System.void</span><span class="sxs-lookup"><span data-stu-id="64a27-130">System.Void</span></span>

## <span data-ttu-id="64a27-131">筆記</span><span class="sxs-lookup"><span data-stu-id="64a27-131">NOTES</span></span>

## <span data-ttu-id="64a27-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="64a27-132">RELATED LINKS</span></span>

[<span data-ttu-id="64a27-133">AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="64a27-133">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="64a27-134">新-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="64a27-134">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="64a27-135">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="64a27-135">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


