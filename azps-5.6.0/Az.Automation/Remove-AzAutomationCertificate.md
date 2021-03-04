---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: 17eb5530511ccc4303fdb2c978006223e6bd7ed5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916674"
---
# <span data-ttu-id="108d3-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="108d3-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="108d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="108d3-102">SYNOPSIS</span></span>
<span data-ttu-id="108d3-103">移除自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="108d3-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="108d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="108d3-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="108d3-105">描述</span><span class="sxs-lookup"><span data-stu-id="108d3-105">DESCRIPTION</span></span>
<span data-ttu-id="108d3-106">**Remove-AzAutomationCertificate** Cmdlet 會從 Azure Automation 移除憑證。</span><span class="sxs-lookup"><span data-stu-id="108d3-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="108d3-107">例子</span><span class="sxs-lookup"><span data-stu-id="108d3-107">EXAMPLES</span></span>

### <span data-ttu-id="108d3-108">範例 1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="108d3-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="108d3-109">此命令會移除自動化帳戶中名為 Contoso17 的憑證 Cert01。</span><span class="sxs-lookup"><span data-stu-id="108d3-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="108d3-110">參數</span><span class="sxs-lookup"><span data-stu-id="108d3-110">PARAMETERS</span></span>

### <span data-ttu-id="108d3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="108d3-111">-AutomationAccountName</span></span>
<span data-ttu-id="108d3-112">指定此 Cmdlet 移除憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="108d3-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="108d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="108d3-113">-DefaultProfile</span></span>
<span data-ttu-id="108d3-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="108d3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="108d3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="108d3-115">-Name</span></span>
<span data-ttu-id="108d3-116">指定此 Cmdlet 移除的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="108d3-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="108d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="108d3-117">-ResourceGroupName</span></span>
<span data-ttu-id="108d3-118">指定此 Cmdlet 移除憑證的資源組名。</span><span class="sxs-lookup"><span data-stu-id="108d3-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="108d3-119">-確認</span><span class="sxs-lookup"><span data-stu-id="108d3-119">-Confirm</span></span>
<span data-ttu-id="108d3-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="108d3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="108d3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="108d3-121">-WhatIf</span></span>
<span data-ttu-id="108d3-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="108d3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="108d3-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="108d3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="108d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108d3-124">CommonParameters</span></span>
<span data-ttu-id="108d3-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="108d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="108d3-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="108d3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108d3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="108d3-127">INPUTS</span></span>

### <span data-ttu-id="108d3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="108d3-128">System.String</span></span>

## <span data-ttu-id="108d3-129">輸出</span><span class="sxs-lookup"><span data-stu-id="108d3-129">OUTPUTS</span></span>

### <span data-ttu-id="108d3-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="108d3-130">System.Void</span></span>

## <span data-ttu-id="108d3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="108d3-131">NOTES</span></span>

## <span data-ttu-id="108d3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="108d3-132">RELATED LINKS</span></span>

[<span data-ttu-id="108d3-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="108d3-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="108d3-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="108d3-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="108d3-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="108d3-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


