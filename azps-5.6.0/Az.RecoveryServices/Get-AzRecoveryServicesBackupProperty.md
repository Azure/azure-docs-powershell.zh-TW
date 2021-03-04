---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 2cabaaedbd384237cd8be1469ea5f28cbc1e951f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909974"
---
# <span data-ttu-id="28aef-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="28aef-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="28aef-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28aef-102">SYNOPSIS</span></span>
<span data-ttu-id="28aef-103">獲得備份屬性。</span><span class="sxs-lookup"><span data-stu-id="28aef-103">Gets Backup properties.</span></span>

## <span data-ttu-id="28aef-104">語法</span><span class="sxs-lookup"><span data-stu-id="28aef-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28aef-105">描述</span><span class="sxs-lookup"><span data-stu-id="28aef-105">DESCRIPTION</span></span>
<span data-ttu-id="28aef-106">**Get-AzRecoveryServicesBackupProperty** Cmdlet 會取得修復服務庫的備份屬性。</span><span class="sxs-lookup"><span data-stu-id="28aef-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="28aef-107">例子</span><span class="sxs-lookup"><span data-stu-id="28aef-107">EXAMPLES</span></span>

### <span data-ttu-id="28aef-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="28aef-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="28aef-109">取得儲存庫的備份庫屬性。</span><span class="sxs-lookup"><span data-stu-id="28aef-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="28aef-110">參數</span><span class="sxs-lookup"><span data-stu-id="28aef-110">PARAMETERS</span></span>

### <span data-ttu-id="28aef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28aef-111">-DefaultProfile</span></span>
<span data-ttu-id="28aef-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28aef-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28aef-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="28aef-113">-Vault</span></span>
<span data-ttu-id="28aef-114">指定儲存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="28aef-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="28aef-115">該庫必須是 **AzureRmRecoveryServicesVault** 物件。</span><span class="sxs-lookup"><span data-stu-id="28aef-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="28aef-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28aef-116">CommonParameters</span></span>
<span data-ttu-id="28aef-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28aef-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28aef-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28aef-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28aef-119">輸入</span><span class="sxs-lookup"><span data-stu-id="28aef-119">INPUTS</span></span>

### <span data-ttu-id="28aef-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="28aef-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="28aef-121">輸出</span><span class="sxs-lookup"><span data-stu-id="28aef-121">OUTPUTS</span></span>

### <span data-ttu-id="28aef-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="28aef-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="28aef-123">筆記</span><span class="sxs-lookup"><span data-stu-id="28aef-123">NOTES</span></span>

## <span data-ttu-id="28aef-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="28aef-124">RELATED LINKS</span></span>
