---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 846c27dc521e13cb2814a4f9e004325da4263bf7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791842"
---
# <span data-ttu-id="a728f-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="a728f-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="a728f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a728f-102">SYNOPSIS</span></span>
<span data-ttu-id="a728f-103">設定要用於在目前 PowerShell 會話中進行後續 Azure 網站恢復作業的復原服務電子倉庫內容。</span><span class="sxs-lookup"><span data-stu-id="a728f-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="a728f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a728f-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a728f-105">說明</span><span class="sxs-lookup"><span data-stu-id="a728f-105">DESCRIPTION</span></span>
<span data-ttu-id="a728f-106">**AzRecoveryServicesAsrVaultCoNtext** Cmdlet 會設定 Azure Site Recovery 保存庫內容以進行進一步的操作。</span><span class="sxs-lookup"><span data-stu-id="a728f-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="a728f-107">示例</span><span class="sxs-lookup"><span data-stu-id="a728f-107">EXAMPLES</span></span>

### <span data-ttu-id="a728f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a728f-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="a728f-109">在目前的 PowerShell 會話中，將保存庫內容設為指定的 [恢復服務] 保存庫，以進行後續的 Azure 網站恢復作業。</span><span class="sxs-lookup"><span data-stu-id="a728f-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="a728f-110">參數</span><span class="sxs-lookup"><span data-stu-id="a728f-110">PARAMETERS</span></span>

### <span data-ttu-id="a728f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a728f-111">-DefaultProfile</span></span>
<span data-ttu-id="a728f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a728f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a728f-113">-保存庫</span><span class="sxs-lookup"><span data-stu-id="a728f-113">-Vault</span></span>
<span data-ttu-id="a728f-114">與 [恢復服務] 保存庫相對應的 [恢復服務] 保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="a728f-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="a728f-115">-確認</span><span class="sxs-lookup"><span data-stu-id="a728f-115">-Confirm</span></span>
<span data-ttu-id="a728f-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a728f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a728f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a728f-117">-WhatIf</span></span>
<span data-ttu-id="a728f-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a728f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a728f-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a728f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a728f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a728f-120">CommonParameters</span></span>
<span data-ttu-id="a728f-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a728f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a728f-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a728f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a728f-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a728f-123">INPUTS</span></span>

### <span data-ttu-id="a728f-124">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a728f-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a728f-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a728f-125">OUTPUTS</span></span>

### <span data-ttu-id="a728f-126">RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="a728f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="a728f-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a728f-127">NOTES</span></span>

## <span data-ttu-id="a728f-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a728f-128">RELATED LINKS</span></span>
