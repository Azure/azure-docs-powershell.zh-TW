---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437267"
---
# <span data-ttu-id="975d7-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="975d7-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="975d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="975d7-102">SYNOPSIS</span></span>
<span data-ttu-id="975d7-103">刪除恢復服務電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="975d7-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="975d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="975d7-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="975d7-105">說明</span><span class="sxs-lookup"><span data-stu-id="975d7-105">DESCRIPTION</span></span>
<span data-ttu-id="975d7-106">**AzRecoveryServicesVault** Cmdlet 會刪除 [恢復服務] 保存庫。</span><span class="sxs-lookup"><span data-stu-id="975d7-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="975d7-107">示例</span><span class="sxs-lookup"><span data-stu-id="975d7-107">EXAMPLES</span></span>

### <span data-ttu-id="975d7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="975d7-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="975d7-109">刪除恢復服務電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="975d7-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="975d7-110">參數</span><span class="sxs-lookup"><span data-stu-id="975d7-110">PARAMETERS</span></span>

### <span data-ttu-id="975d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="975d7-111">-DefaultProfile</span></span>
<span data-ttu-id="975d7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="975d7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="975d7-113">-保存庫</span><span class="sxs-lookup"><span data-stu-id="975d7-113">-Vault</span></span>
<span data-ttu-id="975d7-114">指定 Azure Site Recovery 保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="975d7-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="975d7-115">-確認</span><span class="sxs-lookup"><span data-stu-id="975d7-115">-Confirm</span></span>
<span data-ttu-id="975d7-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="975d7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="975d7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="975d7-117">-WhatIf</span></span>
<span data-ttu-id="975d7-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="975d7-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="975d7-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="975d7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="975d7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="975d7-120">CommonParameters</span></span>
<span data-ttu-id="975d7-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="975d7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="975d7-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="975d7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="975d7-123">輸入</span><span class="sxs-lookup"><span data-stu-id="975d7-123">INPUTS</span></span>

### <span data-ttu-id="975d7-124">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="975d7-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="975d7-125">輸出</span><span class="sxs-lookup"><span data-stu-id="975d7-125">OUTPUTS</span></span>

### <span data-ttu-id="975d7-126">VaultOperationOutput 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="975d7-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="975d7-127">筆記</span><span class="sxs-lookup"><span data-stu-id="975d7-127">NOTES</span></span>

## <span data-ttu-id="975d7-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="975d7-128">RELATED LINKS</span></span>

[<span data-ttu-id="975d7-129">AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="975d7-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="975d7-130">AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="975d7-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="975d7-131">新-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="975d7-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


