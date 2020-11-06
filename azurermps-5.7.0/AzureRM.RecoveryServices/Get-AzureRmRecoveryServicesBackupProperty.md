---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 19e443a4e7bca12a988e3a339fe9d568d81431b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453100"
---
# <span data-ttu-id="fd86a-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="fd86a-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="fd86a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fd86a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd86a-103">取得備份屬性。</span><span class="sxs-lookup"><span data-stu-id="fd86a-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd86a-104">句法</span><span class="sxs-lookup"><span data-stu-id="fd86a-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd86a-105">說明</span><span class="sxs-lookup"><span data-stu-id="fd86a-105">DESCRIPTION</span></span>
<span data-ttu-id="fd86a-106">**AzureRmRecoveryServicesBackupProperty** Cmdlet 會取得恢復服務電子倉庫的備份屬性。</span><span class="sxs-lookup"><span data-stu-id="fd86a-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="fd86a-107">示例</span><span class="sxs-lookup"><span data-stu-id="fd86a-107">EXAMPLES</span></span>

### <span data-ttu-id="fd86a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="fd86a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="fd86a-109">取得保存庫的備份保存庫屬性。</span><span class="sxs-lookup"><span data-stu-id="fd86a-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="fd86a-110">參數</span><span class="sxs-lookup"><span data-stu-id="fd86a-110">PARAMETERS</span></span>

### <span data-ttu-id="fd86a-111">-保存庫</span><span class="sxs-lookup"><span data-stu-id="fd86a-111">-Vault</span></span>
<span data-ttu-id="fd86a-112">指定保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd86a-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="fd86a-113">Vault 必須是 **AzureRmRecoveryServicesVault** 物件。</span><span class="sxs-lookup"><span data-stu-id="fd86a-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd86a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd86a-114">-DefaultProfile</span></span>
<span data-ttu-id="fd86a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd86a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd86a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd86a-116">CommonParameters</span></span>
<span data-ttu-id="fd86a-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fd86a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd86a-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fd86a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd86a-119">輸入</span><span class="sxs-lookup"><span data-stu-id="fd86a-119">INPUTS</span></span>

### <span data-ttu-id="fd86a-120">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fd86a-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="fd86a-121">輸出</span><span class="sxs-lookup"><span data-stu-id="fd86a-121">OUTPUTS</span></span>

### <span data-ttu-id="fd86a-122">ASRVaultBackupProperties 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fd86a-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="fd86a-123">筆記</span><span class="sxs-lookup"><span data-stu-id="fd86a-123">NOTES</span></span>

## <span data-ttu-id="fd86a-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd86a-124">RELATED LINKS</span></span>

