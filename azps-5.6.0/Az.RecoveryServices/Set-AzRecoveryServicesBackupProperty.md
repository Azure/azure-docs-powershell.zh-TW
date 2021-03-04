---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 5e66fc57f6ee9daffde27226bc0321f415cc10d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913742"
---
# <span data-ttu-id="eb1c0-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="eb1c0-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="eb1c0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eb1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="eb1c0-103">設定備份管理的屬性。</span><span class="sxs-lookup"><span data-stu-id="eb1c0-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="eb1c0-104">語法</span><span class="sxs-lookup"><span data-stu-id="eb1c0-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>  [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-EnableCrossRegionRestore] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb1c0-105">描述</span><span class="sxs-lookup"><span data-stu-id="eb1c0-105">DESCRIPTION</span></span>
<span data-ttu-id="eb1c0-106">**Set-AzRecoveryServicesBackupProperty** Cmdlet 會設定修復服務保存庫的備份儲存屬性。</span><span class="sxs-lookup"><span data-stu-id="eb1c0-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="eb1c0-107">例子</span><span class="sxs-lookup"><span data-stu-id="eb1c0-107">EXAMPLES</span></span>

### <span data-ttu-id="eb1c0-108">範例 1：設定保存庫的 GeoRedundant 儲存空間</span><span class="sxs-lookup"><span data-stu-id="eb1c0-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="eb1c0-109">第一個命令會獲得名為 TestVault 的保存庫，然後將它儲存在 $Vault 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="eb1c0-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="eb1c0-110">第二個命令將 $Vault 01 的備份儲存空間設成 GeoRedundant。</span><span class="sxs-lookup"><span data-stu-id="eb1c0-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="eb1c0-111">參數</span><span class="sxs-lookup"><span data-stu-id="eb1c0-111">PARAMETERS</span></span>

### <span data-ttu-id="eb1c0-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="eb1c0-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="eb1c0-113">指定備份儲存空間的備用類型。</span><span class="sxs-lookup"><span data-stu-id="eb1c0-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, ZoneRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb1c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb1c0-114">-DefaultProfile</span></span>
<span data-ttu-id="eb1c0-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb1c0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb1c0-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="eb1c0-116">-Vault</span></span>
<span data-ttu-id="eb1c0-117">指定儲存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb1c0-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="eb1c0-118">該庫必須是 **AzureRmRecoveryServicesVault** 物件。</span><span class="sxs-lookup"><span data-stu-id="eb1c0-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="eb1c0-119">-確認</span><span class="sxs-lookup"><span data-stu-id="eb1c0-119">-Confirm</span></span>
<span data-ttu-id="eb1c0-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eb1c0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb1c0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb1c0-121">-WhatIf</span></span>
<span data-ttu-id="eb1c0-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb1c0-122">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="eb1c0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb1c0-123">CommonParameters</span></span>
<span data-ttu-id="eb1c0-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eb1c0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb1c0-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb1c0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb1c0-126">輸入</span><span class="sxs-lookup"><span data-stu-id="eb1c0-126">INPUTS</span></span>

### <span data-ttu-id="eb1c0-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="eb1c0-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="eb1c0-128">輸出</span><span class="sxs-lookup"><span data-stu-id="eb1c0-128">OUTPUTS</span></span>

### <span data-ttu-id="eb1c0-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="eb1c0-129">System.Void</span></span>

## <span data-ttu-id="eb1c0-130">筆記</span><span class="sxs-lookup"><span data-stu-id="eb1c0-130">NOTES</span></span>

## <span data-ttu-id="eb1c0-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb1c0-131">RELATED LINKS</span></span>

[<span data-ttu-id="eb1c0-132">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="eb1c0-132">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="eb1c0-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="eb1c0-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


