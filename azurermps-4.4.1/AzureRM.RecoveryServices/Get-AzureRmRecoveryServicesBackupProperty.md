---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 3e93df0adfe1e1bc10d5ea74dd189bee60595824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625088"
---
# <span data-ttu-id="f2245-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="f2245-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="f2245-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2245-102">SYNOPSIS</span></span>
<span data-ttu-id="f2245-103">取得備份屬性。</span><span class="sxs-lookup"><span data-stu-id="f2245-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2245-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2245-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2245-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2245-105">DESCRIPTION</span></span>
<span data-ttu-id="f2245-106">**AzureRmRecoveryServicesBackupProperty** Cmdlet 會取得恢復服務電子倉庫的備份屬性。</span><span class="sxs-lookup"><span data-stu-id="f2245-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="f2245-107">示例</span><span class="sxs-lookup"><span data-stu-id="f2245-107">EXAMPLES</span></span>

## <span data-ttu-id="f2245-108">參數</span><span class="sxs-lookup"><span data-stu-id="f2245-108">PARAMETERS</span></span>

### <span data-ttu-id="f2245-109">-保存庫</span><span class="sxs-lookup"><span data-stu-id="f2245-109">-Vault</span></span>
<span data-ttu-id="f2245-110">指定保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2245-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="f2245-111">Vault 必須是 **AzureRmRecoveryServicesVault** 物件。</span><span class="sxs-lookup"><span data-stu-id="f2245-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="f2245-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2245-112">-DefaultProfile</span></span>
<span data-ttu-id="f2245-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2245-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2245-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2245-114">CommonParameters</span></span>
<span data-ttu-id="f2245-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2245-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2245-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2245-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2245-117">輸入</span><span class="sxs-lookup"><span data-stu-id="f2245-117">INPUTS</span></span>

### <span data-ttu-id="f2245-118">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f2245-118">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="f2245-119">輸出</span><span class="sxs-lookup"><span data-stu-id="f2245-119">OUTPUTS</span></span>

### <span data-ttu-id="f2245-120">ASRVaultBackupProperties 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f2245-120">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="f2245-121">筆記</span><span class="sxs-lookup"><span data-stu-id="f2245-121">NOTES</span></span>

## <span data-ttu-id="f2245-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2245-122">RELATED LINKS</span></span>

