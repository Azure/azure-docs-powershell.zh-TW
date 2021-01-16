---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274127"
---
# <span data-ttu-id="69fae-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="69fae-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="69fae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69fae-102">SYNOPSIS</span></span>
<span data-ttu-id="69fae-103">設定要用於在目前 PowerShell 會話中進行後續 Azure 網站恢復作業的復原服務電子倉庫內容。</span><span class="sxs-lookup"><span data-stu-id="69fae-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="69fae-104">句法</span><span class="sxs-lookup"><span data-stu-id="69fae-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69fae-105">說明</span><span class="sxs-lookup"><span data-stu-id="69fae-105">DESCRIPTION</span></span>
<span data-ttu-id="69fae-106">**AzRecoveryServicesAsrVaultCoNtext** Cmdlet 會設定 Azure Site Recovery 保存庫內容以進行進一步的操作。</span><span class="sxs-lookup"><span data-stu-id="69fae-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="69fae-107">示例</span><span class="sxs-lookup"><span data-stu-id="69fae-107">EXAMPLES</span></span>

### <span data-ttu-id="69fae-108">範例1</span><span class="sxs-lookup"><span data-stu-id="69fae-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="69fae-109">在目前的 PowerShell 會話中，將保存庫內容設為指定的 [恢復服務] 保存庫，以進行後續的 Azure 網站恢復作業。</span><span class="sxs-lookup"><span data-stu-id="69fae-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="69fae-110">參數</span><span class="sxs-lookup"><span data-stu-id="69fae-110">PARAMETERS</span></span>

### <span data-ttu-id="69fae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69fae-111">-DefaultProfile</span></span>
<span data-ttu-id="69fae-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69fae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69fae-113">-保存庫</span><span class="sxs-lookup"><span data-stu-id="69fae-113">-Vault</span></span>
<span data-ttu-id="69fae-114">與 [恢復服務] 保存庫相對應的 [恢復服務] 保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="69fae-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69fae-115">-確認</span><span class="sxs-lookup"><span data-stu-id="69fae-115">-Confirm</span></span>
<span data-ttu-id="69fae-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="69fae-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69fae-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69fae-117">-WhatIf</span></span>
<span data-ttu-id="69fae-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69fae-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69fae-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69fae-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69fae-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69fae-120">CommonParameters</span></span>
<span data-ttu-id="69fae-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69fae-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69fae-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="69fae-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69fae-123">輸入</span><span class="sxs-lookup"><span data-stu-id="69fae-123">INPUTS</span></span>

### <span data-ttu-id="69fae-124">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="69fae-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="69fae-125">輸出</span><span class="sxs-lookup"><span data-stu-id="69fae-125">OUTPUTS</span></span>

### <span data-ttu-id="69fae-126">RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="69fae-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="69fae-127">筆記</span><span class="sxs-lookup"><span data-stu-id="69fae-127">NOTES</span></span>

## <span data-ttu-id="69fae-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="69fae-128">RELATED LINKS</span></span>
