---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: a0f21fc8cde4c64eaf1e8ea27bf05eff8d664c55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791845"
---
# <span data-ttu-id="03144-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="03144-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="03144-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03144-102">SYNOPSIS</span></span>
<span data-ttu-id="03144-103">刪除恢復服務電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="03144-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="03144-104">句法</span><span class="sxs-lookup"><span data-stu-id="03144-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03144-105">說明</span><span class="sxs-lookup"><span data-stu-id="03144-105">DESCRIPTION</span></span>
<span data-ttu-id="03144-106">**AzRecoveryServicesVault** Cmdlet 會刪除 [恢復服務] 保存庫。</span><span class="sxs-lookup"><span data-stu-id="03144-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="03144-107">示例</span><span class="sxs-lookup"><span data-stu-id="03144-107">EXAMPLES</span></span>

### <span data-ttu-id="03144-108">範例1</span><span class="sxs-lookup"><span data-stu-id="03144-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="03144-109">刪除恢復服務電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="03144-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="03144-110">參數</span><span class="sxs-lookup"><span data-stu-id="03144-110">PARAMETERS</span></span>

### <span data-ttu-id="03144-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03144-111">-DefaultProfile</span></span>
<span data-ttu-id="03144-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="03144-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03144-113">-保存庫</span><span class="sxs-lookup"><span data-stu-id="03144-113">-Vault</span></span>
<span data-ttu-id="03144-114">指定 Azure Site Recovery 保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="03144-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="03144-115">-確認</span><span class="sxs-lookup"><span data-stu-id="03144-115">-Confirm</span></span>
<span data-ttu-id="03144-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="03144-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03144-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03144-117">-WhatIf</span></span>
<span data-ttu-id="03144-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03144-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03144-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03144-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03144-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03144-120">CommonParameters</span></span>
<span data-ttu-id="03144-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03144-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03144-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03144-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03144-123">輸入</span><span class="sxs-lookup"><span data-stu-id="03144-123">INPUTS</span></span>

### <span data-ttu-id="03144-124">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="03144-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="03144-125">輸出</span><span class="sxs-lookup"><span data-stu-id="03144-125">OUTPUTS</span></span>

### <span data-ttu-id="03144-126">VaultOperationOutput 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="03144-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="03144-127">筆記</span><span class="sxs-lookup"><span data-stu-id="03144-127">NOTES</span></span>

## <span data-ttu-id="03144-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="03144-128">RELATED LINKS</span></span>

[<span data-ttu-id="03144-129">AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="03144-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="03144-130">AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="03144-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="03144-131">新-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="03144-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

