---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 27b783234f9f38f7445940ceb9969b6bc7fb6273
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139125"
---
# <span data-ttu-id="9e5c8-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="9e5c8-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="9e5c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="9e5c8-103">設定備份管理的屬性。</span><span class="sxs-lookup"><span data-stu-id="9e5c8-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="9e5c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e5c8-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e5c8-105">說明</span><span class="sxs-lookup"><span data-stu-id="9e5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="9e5c8-106">**AzRecoveryServicesBackupProperty** Cmdlet 會為復原服務電子倉庫設定備份儲存空間屬性。</span><span class="sxs-lookup"><span data-stu-id="9e5c8-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="9e5c8-107">示例</span><span class="sxs-lookup"><span data-stu-id="9e5c8-107">EXAMPLES</span></span>

### <span data-ttu-id="9e5c8-108">範例1：為電子倉庫設定 GeoRedundant 儲存空間</span><span class="sxs-lookup"><span data-stu-id="9e5c8-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="9e5c8-109">第一個命令會取得名為 TestVault 的電子倉庫，然後將它儲存在 $Vault 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="9e5c8-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="9e5c8-110">第二個命令會將 $Vault 01 的備份儲存空間冗余設定為 GeoRedundant。</span><span class="sxs-lookup"><span data-stu-id="9e5c8-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="9e5c8-111">參數</span><span class="sxs-lookup"><span data-stu-id="9e5c8-111">PARAMETERS</span></span>

### <span data-ttu-id="9e5c8-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="9e5c8-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="9e5c8-113">指定備份儲存空間複製類型。</span><span class="sxs-lookup"><span data-stu-id="9e5c8-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e5c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e5c8-114">-DefaultProfile</span></span>
<span data-ttu-id="9e5c8-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e5c8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e5c8-116">-保存庫</span><span class="sxs-lookup"><span data-stu-id="9e5c8-116">-Vault</span></span>
<span data-ttu-id="9e5c8-117">指定保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e5c8-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="9e5c8-118">Vault 必須是 **AzureRmRecoveryServicesVault** 物件。</span><span class="sxs-lookup"><span data-stu-id="9e5c8-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="9e5c8-119">-確認</span><span class="sxs-lookup"><span data-stu-id="9e5c8-119">-Confirm</span></span>
<span data-ttu-id="9e5c8-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e5c8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e5c8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e5c8-121">-WhatIf</span></span>
<span data-ttu-id="9e5c8-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e5c8-122">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="9e5c8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e5c8-123">CommonParameters</span></span>
<span data-ttu-id="9e5c8-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e5c8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e5c8-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9e5c8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e5c8-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9e5c8-126">INPUTS</span></span>

### <span data-ttu-id="9e5c8-127">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9e5c8-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="9e5c8-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9e5c8-128">OUTPUTS</span></span>

### <span data-ttu-id="9e5c8-129">System.void</span><span class="sxs-lookup"><span data-stu-id="9e5c8-129">System.Void</span></span>

## <span data-ttu-id="9e5c8-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9e5c8-130">NOTES</span></span>

## <span data-ttu-id="9e5c8-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e5c8-131">RELATED LINKS</span></span>

[<span data-ttu-id="9e5c8-132">AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="9e5c8-132">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="9e5c8-133">AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9e5c8-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


