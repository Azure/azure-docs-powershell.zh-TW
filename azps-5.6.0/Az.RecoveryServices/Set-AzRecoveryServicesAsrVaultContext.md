---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: ad4fe186a07adb2b9f90222d3caf8def1ecbefdc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913749"
---
# <span data-ttu-id="9af48-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="9af48-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="9af48-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9af48-102">SYNOPSIS</span></span>
<span data-ttu-id="9af48-103">設定要用於目前 PowerShell 會話中後續 Azure 網站復原作業的修復服務庫上下文。</span><span class="sxs-lookup"><span data-stu-id="9af48-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="9af48-104">語法</span><span class="sxs-lookup"><span data-stu-id="9af48-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9af48-105">描述</span><span class="sxs-lookup"><span data-stu-id="9af48-105">DESCRIPTION</span></span>
<span data-ttu-id="9af48-106">**Set-AzRecoveryServicesAsrVaultCoNtext** Cmdlet 會設定 Azure 網站復原庫上下文，以進一步操作。</span><span class="sxs-lookup"><span data-stu-id="9af48-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="9af48-107">例子</span><span class="sxs-lookup"><span data-stu-id="9af48-107">EXAMPLES</span></span>

### <span data-ttu-id="9af48-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9af48-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="9af48-109">針對目前 PowerShell 會話中的後續 Azure 網站復原作業，將儲存庫上下文設定為指定的修復服務儲存庫。</span><span class="sxs-lookup"><span data-stu-id="9af48-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="9af48-110">參數</span><span class="sxs-lookup"><span data-stu-id="9af48-110">PARAMETERS</span></span>

### <span data-ttu-id="9af48-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af48-111">-DefaultProfile</span></span>
<span data-ttu-id="9af48-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9af48-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9af48-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="9af48-113">-Vault</span></span>
<span data-ttu-id="9af48-114">對應至修復服務儲存庫的修復服務庫物件。</span><span class="sxs-lookup"><span data-stu-id="9af48-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="9af48-115">-確認</span><span class="sxs-lookup"><span data-stu-id="9af48-115">-Confirm</span></span>
<span data-ttu-id="9af48-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9af48-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9af48-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9af48-117">-WhatIf</span></span>
<span data-ttu-id="9af48-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9af48-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9af48-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9af48-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9af48-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af48-120">CommonParameters</span></span>
<span data-ttu-id="9af48-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9af48-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af48-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9af48-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af48-123">輸入</span><span class="sxs-lookup"><span data-stu-id="9af48-123">INPUTS</span></span>

### <span data-ttu-id="9af48-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="9af48-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="9af48-125">輸出</span><span class="sxs-lookup"><span data-stu-id="9af48-125">OUTPUTS</span></span>

### <span data-ttu-id="9af48-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="9af48-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="9af48-127">筆記</span><span class="sxs-lookup"><span data-stu-id="9af48-127">NOTES</span></span>

## <span data-ttu-id="9af48-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="9af48-128">RELATED LINKS</span></span>
