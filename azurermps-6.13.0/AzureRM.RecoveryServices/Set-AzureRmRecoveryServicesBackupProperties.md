---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesbackupproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
ms.openlocfilehash: 7fa55bd306a1cbe04ddf3af63a66682a0fa17f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445520"
---
# <span data-ttu-id="491e4-101">Set-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="491e4-101">Set-AzureRmRecoveryServicesBackupProperties</span></span>

## <span data-ttu-id="491e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="491e4-102">SYNOPSIS</span></span>
<span data-ttu-id="491e4-103">設定備份管理的屬性。</span><span class="sxs-lookup"><span data-stu-id="491e4-103">Sets the properties for backup management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="491e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="491e4-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProperties -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="491e4-105">說明</span><span class="sxs-lookup"><span data-stu-id="491e4-105">DESCRIPTION</span></span>
<span data-ttu-id="491e4-106">**AzureRmRecoveryServicesBackupProperties** Cmdlet 會為復原服務電子倉庫設定備份儲存空間屬性。</span><span class="sxs-lookup"><span data-stu-id="491e4-106">The **Set-AzureRmRecoveryServicesBackupProperties** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="491e4-107">示例</span><span class="sxs-lookup"><span data-stu-id="491e4-107">EXAMPLES</span></span>

### <span data-ttu-id="491e4-108">範例1：為電子倉庫設定 GeoRedundant 儲存空間</span><span class="sxs-lookup"><span data-stu-id="491e4-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzureRmRecoveryServicesBackupProperties -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="491e4-109">第一個命令會取得名為 TestVault 的電子倉庫，然後將它儲存在 $Vault 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="491e4-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="491e4-110">第二個命令會將 $Vault 01 的備份儲存空間冗余設定為 GeoRedundant。</span><span class="sxs-lookup"><span data-stu-id="491e4-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="491e4-111">參數</span><span class="sxs-lookup"><span data-stu-id="491e4-111">PARAMETERS</span></span>

### <span data-ttu-id="491e4-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="491e4-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="491e4-113">指定備份儲存空間複製類型。</span><span class="sxs-lookup"><span data-stu-id="491e4-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: AzureRmRecoveryServicesBackupStorageRedundancyType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="491e4-114">-保存庫</span><span class="sxs-lookup"><span data-stu-id="491e4-114">-Vault</span></span>
<span data-ttu-id="491e4-115">指定保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="491e4-115">Specifies the name of the vault.</span></span>
<span data-ttu-id="491e4-116">Vault 必須是 **AzureRmRecoveryServicesVault** 物件。</span><span class="sxs-lookup"><span data-stu-id="491e4-116">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="491e4-117">-確認</span><span class="sxs-lookup"><span data-stu-id="491e4-117">-Confirm</span></span>
<span data-ttu-id="491e4-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="491e4-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="491e4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="491e4-119">-WhatIf</span></span>
<span data-ttu-id="491e4-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="491e4-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="491e4-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="491e4-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="491e4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="491e4-122">-DefaultProfile</span></span>
<span data-ttu-id="491e4-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="491e4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="491e4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="491e4-124">CommonParameters</span></span>
<span data-ttu-id="491e4-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="491e4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="491e4-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="491e4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="491e4-127">輸入</span><span class="sxs-lookup"><span data-stu-id="491e4-127">INPUTS</span></span>

### <span data-ttu-id="491e4-128">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="491e4-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="491e4-129">參數：保存庫 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="491e4-129">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="491e4-130">輸出</span><span class="sxs-lookup"><span data-stu-id="491e4-130">OUTPUTS</span></span>

### <span data-ttu-id="491e4-131">System.void</span><span class="sxs-lookup"><span data-stu-id="491e4-131">System.Void</span></span>

## <span data-ttu-id="491e4-132">筆記</span><span class="sxs-lookup"><span data-stu-id="491e4-132">NOTES</span></span>

## <span data-ttu-id="491e4-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="491e4-133">RELATED LINKS</span></span>

[<span data-ttu-id="491e4-134">AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="491e4-134">Get-AzureRmRecoveryServicesBackupProperties</span></span>](./Get-AzureRmRecoveryServicesBackupProperties.md)

[<span data-ttu-id="491e4-135">AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="491e4-135">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)


