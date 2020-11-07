---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
ms.openlocfilehash: 00d7bb2c58abfa466b0c4843eb480b43b08b3d90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625261"
---
# <span data-ttu-id="be103-101">Get-AzureRmRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="be103-101">Get-AzureRmRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="be103-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be103-102">SYNOPSIS</span></span>
<span data-ttu-id="be103-103">檢查您的 ARM 資源是否已備份。</span><span class="sxs-lookup"><span data-stu-id="be103-103">Checks whether your ARM resource is backed up or not.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be103-104">句法</span><span class="sxs-lookup"><span data-stu-id="be103-104">SYNTAX</span></span>

### <span data-ttu-id="be103-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="be103-105">Name (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be103-106">標識號</span><span class="sxs-lookup"><span data-stu-id="be103-106">Id</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be103-107">說明</span><span class="sxs-lookup"><span data-stu-id="be103-107">DESCRIPTION</span></span>
<span data-ttu-id="be103-108">如果指定的資源未在訂閱中的任何復原服務電子倉庫中受到保護，此命令就會傳回 null/空。</span><span class="sxs-lookup"><span data-stu-id="be103-108">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="be103-109">如果受保護，則會傳回相關的保存庫詳細資料。</span><span class="sxs-lookup"><span data-stu-id="be103-109">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="be103-110">示例</span><span class="sxs-lookup"><span data-stu-id="be103-110">EXAMPLES</span></span>

### <span data-ttu-id="be103-111">範例1</span><span class="sxs-lookup"><span data-stu-id="be103-111">Example 1</span></span>
```
PS C:\> $status = Get-AzureRmRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzureRmRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzureRmRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="be103-112">參數</span><span class="sxs-lookup"><span data-stu-id="be103-112">PARAMETERS</span></span>

### <span data-ttu-id="be103-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be103-113">-DefaultProfile</span></span>
<span data-ttu-id="be103-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be103-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be103-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="be103-115">-Name</span></span>
<span data-ttu-id="be103-116">需要檢查其代表代表的 Azure 資源的名稱（如果訂閱中的某些復原服務電子倉庫已受保護）。</span><span class="sxs-lookup"><span data-stu-id="be103-116">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="be103-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be103-117">-ResourceGroupName</span></span>
<span data-ttu-id="be103-118">Azure 資源的資源群組名稱，其代表者必須核取該資源，且該資源已由訂閱中的某些 RecoveryServices Vault 所保護。</span><span class="sxs-lookup"><span data-stu-id="be103-118">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="be103-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be103-119">-ResourceId</span></span>
<span data-ttu-id="be103-120">需要檢查其代表代表的 Azure 資源（如果訂閱中的某些 RecoveryServices 保存庫已受到保護）的 ID。</span><span class="sxs-lookup"><span data-stu-id="be103-120">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be103-121">-類型</span><span class="sxs-lookup"><span data-stu-id="be103-121">-Type</span></span>
<span data-ttu-id="be103-122">需要檢查其代表代表的 Azure 資源的名稱（如果訂閱中的某些復原服務電子倉庫已受保護）。</span><span class="sxs-lookup"><span data-stu-id="be103-122">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be103-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be103-123">CommonParameters</span></span>
<span data-ttu-id="be103-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be103-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be103-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be103-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be103-126">輸入</span><span class="sxs-lookup"><span data-stu-id="be103-126">INPUTS</span></span>

### <span data-ttu-id="be103-127">System.object</span><span class="sxs-lookup"><span data-stu-id="be103-127">System.String</span></span>

## <span data-ttu-id="be103-128">輸出</span><span class="sxs-lookup"><span data-stu-id="be103-128">OUTPUTS</span></span>

### <span data-ttu-id="be103-129">ResourceBackupStatus 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="be103-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="be103-130">筆記</span><span class="sxs-lookup"><span data-stu-id="be103-130">NOTES</span></span>

## <span data-ttu-id="be103-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="be103-131">RELATED LINKS</span></span>
