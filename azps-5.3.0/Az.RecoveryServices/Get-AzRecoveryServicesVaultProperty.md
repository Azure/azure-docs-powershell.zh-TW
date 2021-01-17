---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: da541e9f019dfb82efc496ce60ab300229e36ac0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436243"
---
# <span data-ttu-id="18b9d-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="18b9d-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="18b9d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="18b9d-103">傳回恢復服務保存庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="18b9d-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="18b9d-104">句法</span><span class="sxs-lookup"><span data-stu-id="18b9d-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18b9d-105">說明</span><span class="sxs-lookup"><span data-stu-id="18b9d-105">DESCRIPTION</span></span>
<span data-ttu-id="18b9d-106">**AzRecoveryServicesVaultProperty** Cmdlet 會傳回恢復服務保存庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="18b9d-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="18b9d-107">示例</span><span class="sxs-lookup"><span data-stu-id="18b9d-107">EXAMPLES</span></span>

### <span data-ttu-id="18b9d-108">範例1：取得保存庫的屬性</span><span class="sxs-lookup"><span data-stu-id="18b9d-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="18b9d-109">第一個命令會取得 Vault 物件，然後將它儲存在 $vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="18b9d-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="18b9d-110">第二個命令會取得保存庫屬性。</span><span class="sxs-lookup"><span data-stu-id="18b9d-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="18b9d-111">接下來，我們將存取電子倉庫的 encryptionProperties。</span><span class="sxs-lookup"><span data-stu-id="18b9d-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="18b9d-112">參數</span><span class="sxs-lookup"><span data-stu-id="18b9d-112">PARAMETERS</span></span>

### <span data-ttu-id="18b9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b9d-113">-DefaultProfile</span></span>
<span data-ttu-id="18b9d-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="18b9d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18b9d-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="18b9d-115">-VaultId</span></span>
<span data-ttu-id="18b9d-116">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="18b9d-116">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="18b9d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b9d-117">CommonParameters</span></span>
<span data-ttu-id="18b9d-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18b9d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b9d-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="18b9d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b9d-120">輸入</span><span class="sxs-lookup"><span data-stu-id="18b9d-120">INPUTS</span></span>

### <span data-ttu-id="18b9d-121">System.object</span><span class="sxs-lookup"><span data-stu-id="18b9d-121">System.String</span></span>

## <span data-ttu-id="18b9d-122">輸出</span><span class="sxs-lookup"><span data-stu-id="18b9d-122">OUTPUTS</span></span>

### <span data-ttu-id="18b9d-123">BackupResourceVaultConfigResource 中的 RecoveryServices 備份。</span><span class="sxs-lookup"><span data-stu-id="18b9d-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="18b9d-124">筆記</span><span class="sxs-lookup"><span data-stu-id="18b9d-124">NOTES</span></span>

## <span data-ttu-id="18b9d-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="18b9d-125">RELATED LINKS</span></span>

[<span data-ttu-id="18b9d-126">AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="18b9d-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="18b9d-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="18b9d-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
