---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: b3d0b292d7e680ca1d16e935c34a268cea836aeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902201"
---
# <span data-ttu-id="50aed-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="50aed-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="50aed-102">簡介</span><span class="sxs-lookup"><span data-stu-id="50aed-102">SYNOPSIS</span></span>
<span data-ttu-id="50aed-103">刪除修復服務儲存庫。</span><span class="sxs-lookup"><span data-stu-id="50aed-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="50aed-104">語法</span><span class="sxs-lookup"><span data-stu-id="50aed-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50aed-105">描述</span><span class="sxs-lookup"><span data-stu-id="50aed-105">DESCRIPTION</span></span>
<span data-ttu-id="50aed-106">**Remove-AzRecoveryServicesVault** Cmdlet 會刪除修復服務庫。</span><span class="sxs-lookup"><span data-stu-id="50aed-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="50aed-107">例子</span><span class="sxs-lookup"><span data-stu-id="50aed-107">EXAMPLES</span></span>

### <span data-ttu-id="50aed-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="50aed-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="50aed-109">刪除修復服務儲存庫。</span><span class="sxs-lookup"><span data-stu-id="50aed-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="50aed-110">參數</span><span class="sxs-lookup"><span data-stu-id="50aed-110">PARAMETERS</span></span>

### <span data-ttu-id="50aed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50aed-111">-DefaultProfile</span></span>
<span data-ttu-id="50aed-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="50aed-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50aed-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="50aed-113">-Vault</span></span>
<span data-ttu-id="50aed-114">指定 Azure 網站修復庫物件。</span><span class="sxs-lookup"><span data-stu-id="50aed-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="50aed-115">-確認</span><span class="sxs-lookup"><span data-stu-id="50aed-115">-Confirm</span></span>
<span data-ttu-id="50aed-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="50aed-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50aed-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50aed-117">-WhatIf</span></span>
<span data-ttu-id="50aed-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50aed-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50aed-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50aed-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50aed-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50aed-120">CommonParameters</span></span>
<span data-ttu-id="50aed-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="50aed-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50aed-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50aed-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50aed-123">輸入</span><span class="sxs-lookup"><span data-stu-id="50aed-123">INPUTS</span></span>

### <span data-ttu-id="50aed-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="50aed-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="50aed-125">輸出</span><span class="sxs-lookup"><span data-stu-id="50aed-125">OUTPUTS</span></span>

### <span data-ttu-id="50aed-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="50aed-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="50aed-127">筆記</span><span class="sxs-lookup"><span data-stu-id="50aed-127">NOTES</span></span>

## <span data-ttu-id="50aed-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="50aed-128">RELATED LINKS</span></span>

[<span data-ttu-id="50aed-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="50aed-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="50aed-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="50aed-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="50aed-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="50aed-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


