---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
ms.openlocfilehash: 1e10fe2aa534e236c99468ec672e6a0eeadae469
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966165"
---
# <span data-ttu-id="da4b5-101">Get-AzRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="da4b5-101">Get-AzRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="da4b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da4b5-102">SYNOPSIS</span></span>
<span data-ttu-id="da4b5-103">檢查您的 ARM 資源是否已備份。</span><span class="sxs-lookup"><span data-stu-id="da4b5-103">Checks whether your ARM resource is backed up or not.</span></span>

## <span data-ttu-id="da4b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="da4b5-104">SYNTAX</span></span>

### <span data-ttu-id="da4b5-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="da4b5-105">Name (Default)</span></span>
```
Get-AzRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da4b5-106">IdWorkload</span><span class="sxs-lookup"><span data-stu-id="da4b5-106">IdWorkload</span></span>
```
Get-AzRecoveryServicesBackupStatus -Type <String> -ResourceId <String> -ProtectableObjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da4b5-107">標識號</span><span class="sxs-lookup"><span data-stu-id="da4b5-107">Id</span></span>
```
Get-AzRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da4b5-108">說明</span><span class="sxs-lookup"><span data-stu-id="da4b5-108">DESCRIPTION</span></span>
<span data-ttu-id="da4b5-109">如果指定的資源未在訂閱中的任何復原服務電子倉庫中受到保護，此命令就會傳回 null/空。</span><span class="sxs-lookup"><span data-stu-id="da4b5-109">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="da4b5-110">如果受保護，則會傳回相關的保存庫詳細資料。</span><span class="sxs-lookup"><span data-stu-id="da4b5-110">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="da4b5-111">示例</span><span class="sxs-lookup"><span data-stu-id="da4b5-111">EXAMPLES</span></span>

### <span data-ttu-id="da4b5-112">範例1</span><span class="sxs-lookup"><span data-stu-id="da4b5-112">Example 1</span></span>
```
PS C:\> $status = Get-AzRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="da4b5-113">參數</span><span class="sxs-lookup"><span data-stu-id="da4b5-113">PARAMETERS</span></span>

### <span data-ttu-id="da4b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da4b5-114">-DefaultProfile</span></span>
<span data-ttu-id="da4b5-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="da4b5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da4b5-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="da4b5-116">-Name</span></span>
<span data-ttu-id="da4b5-117">需要檢查其代表代表的 Azure 資源的名稱（如果訂閱中的某些復原服務電子倉庫已受保護）。</span><span class="sxs-lookup"><span data-stu-id="da4b5-117">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4b5-118">-ProtectableObjectName</span><span class="sxs-lookup"><span data-stu-id="da4b5-118">-ProtectableObjectName</span></span>
<span data-ttu-id="da4b5-119">需要檢查其代表代表的 Azure 資源的名稱（如果訂閱中的某些復原服務電子倉庫已受保護）。</span><span class="sxs-lookup"><span data-stu-id="da4b5-119">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da4b5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da4b5-120">-ResourceGroupName</span></span>
<span data-ttu-id="da4b5-121">Azure 資源的資源群組名稱，其代表者必須核取該資源，且該資源已由訂閱中的某些 RecoveryServices Vault 所保護。</span><span class="sxs-lookup"><span data-stu-id="da4b5-121">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4b5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da4b5-122">-ResourceId</span></span>
<span data-ttu-id="da4b5-123">需要檢查其代表代表的 Azure 資源（如果訂閱中的某些 RecoveryServices 保存庫已受到保護）的 ID。</span><span class="sxs-lookup"><span data-stu-id="da4b5-123">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload, Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da4b5-124">-類型</span><span class="sxs-lookup"><span data-stu-id="da4b5-124">-Type</span></span>
<span data-ttu-id="da4b5-125">需要檢查其代表代表的 Azure 資源的名稱（如果訂閱中的某些復原服務電子倉庫已受保護）。</span><span class="sxs-lookup"><span data-stu-id="da4b5-125">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, IdWorkload
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4b5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da4b5-126">CommonParameters</span></span>
<span data-ttu-id="da4b5-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da4b5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da4b5-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="da4b5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da4b5-129">輸入</span><span class="sxs-lookup"><span data-stu-id="da4b5-129">INPUTS</span></span>

### <span data-ttu-id="da4b5-130">System.object</span><span class="sxs-lookup"><span data-stu-id="da4b5-130">System.String</span></span>

## <span data-ttu-id="da4b5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="da4b5-131">OUTPUTS</span></span>

### <span data-ttu-id="da4b5-132">ResourceBackupStatus 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="da4b5-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="da4b5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="da4b5-133">NOTES</span></span>

## <span data-ttu-id="da4b5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="da4b5-134">RELATED LINKS</span></span>
