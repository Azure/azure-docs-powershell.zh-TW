---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4e0b74ead08a3b944e66b46a6fee0fb71976b223
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907333"
---
# <span data-ttu-id="20271-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="20271-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="20271-102">簡介</span><span class="sxs-lookup"><span data-stu-id="20271-102">SYNOPSIS</span></span>
<span data-ttu-id="20271-103">會返回修復服務儲存庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="20271-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="20271-104">語法</span><span class="sxs-lookup"><span data-stu-id="20271-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20271-105">描述</span><span class="sxs-lookup"><span data-stu-id="20271-105">DESCRIPTION</span></span>
<span data-ttu-id="20271-106">**Get-AzRecoveryServicesVaultProperty** Cmdlet 會返回修復服務庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="20271-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="20271-107">例子</span><span class="sxs-lookup"><span data-stu-id="20271-107">EXAMPLES</span></span>

### <span data-ttu-id="20271-108">範例 1：取得儲存庫的屬性</span><span class="sxs-lookup"><span data-stu-id="20271-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="20271-109">第一個命令會獲得保存庫物件，然後將它儲存在$vault變數中。</span><span class="sxs-lookup"><span data-stu-id="20271-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="20271-110">第二個命令會獲得儲存庫屬性。</span><span class="sxs-lookup"><span data-stu-id="20271-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="20271-111">接下來，我們存取該儲存庫的加密Properties。</span><span class="sxs-lookup"><span data-stu-id="20271-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="20271-112">參數</span><span class="sxs-lookup"><span data-stu-id="20271-112">PARAMETERS</span></span>

### <span data-ttu-id="20271-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20271-113">-DefaultProfile</span></span>
<span data-ttu-id="20271-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="20271-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20271-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="20271-115">-VaultId</span></span>
<span data-ttu-id="20271-116">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="20271-116">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20271-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20271-117">CommonParameters</span></span>
<span data-ttu-id="20271-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="20271-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20271-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20271-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20271-120">輸入</span><span class="sxs-lookup"><span data-stu-id="20271-120">INPUTS</span></span>

### <span data-ttu-id="20271-121">System.String</span><span class="sxs-lookup"><span data-stu-id="20271-121">System.String</span></span>

## <span data-ttu-id="20271-122">輸出</span><span class="sxs-lookup"><span data-stu-id="20271-122">OUTPUTS</span></span>

### <span data-ttu-id="20271-123">Microsoft.Azure.management.RecoveryServices.Backup.models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="20271-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="20271-124">筆記</span><span class="sxs-lookup"><span data-stu-id="20271-124">NOTES</span></span>

## <span data-ttu-id="20271-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="20271-125">RELATED LINKS</span></span>

[<span data-ttu-id="20271-126">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="20271-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="20271-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="20271-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
