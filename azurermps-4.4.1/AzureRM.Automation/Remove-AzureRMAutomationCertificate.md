---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: d1230030f95d22d972aa537208b30f350ec9dbe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450895"
---
# <span data-ttu-id="60fcb-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="60fcb-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="60fcb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="60fcb-103">移除自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="60fcb-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60fcb-104">句法</span><span class="sxs-lookup"><span data-stu-id="60fcb-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60fcb-105">說明</span><span class="sxs-lookup"><span data-stu-id="60fcb-105">DESCRIPTION</span></span>
<span data-ttu-id="60fcb-106">**AzureRmAutomationCertificate** Cmdlet 會從 Azure 自動化中移除證書。</span><span class="sxs-lookup"><span data-stu-id="60fcb-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="60fcb-107">示例</span><span class="sxs-lookup"><span data-stu-id="60fcb-107">EXAMPLES</span></span>

### <span data-ttu-id="60fcb-108">範例1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="60fcb-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="60fcb-109">這個命令會在名為 [Contoso17] 的自動化帳戶中移除名為 Cert01 的憑證。</span><span class="sxs-lookup"><span data-stu-id="60fcb-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="60fcb-110">參數</span><span class="sxs-lookup"><span data-stu-id="60fcb-110">PARAMETERS</span></span>

### <span data-ttu-id="60fcb-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="60fcb-111">-AutomationAccountName</span></span>
<span data-ttu-id="60fcb-112">指定此 Cmdlet 移除憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="60fcb-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="60fcb-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="60fcb-113">-Name</span></span>
<span data-ttu-id="60fcb-114">指定此 Cmdlet 移除之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="60fcb-114">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="60fcb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60fcb-115">-ResourceGroupName</span></span>
<span data-ttu-id="60fcb-116">指定此 Cmdlet 移除憑證的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="60fcb-116">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="60fcb-117">-確認</span><span class="sxs-lookup"><span data-stu-id="60fcb-117">-Confirm</span></span>
<span data-ttu-id="60fcb-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60fcb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60fcb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60fcb-119">-WhatIf</span></span>
<span data-ttu-id="60fcb-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60fcb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60fcb-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60fcb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60fcb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60fcb-122">-DefaultProfile</span></span>
<span data-ttu-id="60fcb-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60fcb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60fcb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60fcb-124">CommonParameters</span></span>
<span data-ttu-id="60fcb-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60fcb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60fcb-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60fcb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60fcb-127">輸入</span><span class="sxs-lookup"><span data-stu-id="60fcb-127">INPUTS</span></span>

## <span data-ttu-id="60fcb-128">輸出</span><span class="sxs-lookup"><span data-stu-id="60fcb-128">OUTPUTS</span></span>

## <span data-ttu-id="60fcb-129">筆記</span><span class="sxs-lookup"><span data-stu-id="60fcb-129">NOTES</span></span>

## <span data-ttu-id="60fcb-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="60fcb-130">RELATED LINKS</span></span>

[<span data-ttu-id="60fcb-131">AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="60fcb-131">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="60fcb-132">新-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="60fcb-132">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="60fcb-133">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="60fcb-133">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


