---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 811ac8b9f8922844dd5153a4fa02abc4c023f7a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902249"
---
# <span data-ttu-id="ef489-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ef489-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="ef489-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ef489-102">SYNOPSIS</span></span>
<span data-ttu-id="ef489-103">建立新的修復服務儲存庫。</span><span class="sxs-lookup"><span data-stu-id="ef489-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="ef489-104">語法</span><span class="sxs-lookup"><span data-stu-id="ef489-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef489-105">描述</span><span class="sxs-lookup"><span data-stu-id="ef489-105">DESCRIPTION</span></span>
<span data-ttu-id="ef489-106">**New-AzRecoveryServicesVault** Cmdlet 會建立新的修復服務儲存庫。</span><span class="sxs-lookup"><span data-stu-id="ef489-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="ef489-107">例子</span><span class="sxs-lookup"><span data-stu-id="ef489-107">EXAMPLES</span></span>

### <span data-ttu-id="ef489-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="ef489-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="ef489-109">在資源群組和指定位置中建立復原服務庫。</span><span class="sxs-lookup"><span data-stu-id="ef489-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="ef489-110">參數</span><span class="sxs-lookup"><span data-stu-id="ef489-110">PARAMETERS</span></span>

### <span data-ttu-id="ef489-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef489-111">-DefaultProfile</span></span>
<span data-ttu-id="ef489-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef489-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef489-113">-位置</span><span class="sxs-lookup"><span data-stu-id="ef489-113">-Location</span></span>
<span data-ttu-id="ef489-114">指定庫的地理位置名稱。</span><span class="sxs-lookup"><span data-stu-id="ef489-114">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef489-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef489-115">-Name</span></span>
<span data-ttu-id="ef489-116">指定要建立之儲存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef489-116">Specifies the name of the vault to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef489-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef489-117">-ResourceGroupName</span></span>
<span data-ttu-id="ef489-118">指定要建立或用於取回指定修復服務物件的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="ef489-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef489-119">-標記</span><span class="sxs-lookup"><span data-stu-id="ef489-119">-Tag</span></span>

<span data-ttu-id="ef489-120">指定要新加到修復服務庫的標記</span><span class="sxs-lookup"><span data-stu-id="ef489-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef489-121">-確認</span><span class="sxs-lookup"><span data-stu-id="ef489-121">-Confirm</span></span>
<span data-ttu-id="ef489-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ef489-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef489-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef489-123">-WhatIf</span></span>
<span data-ttu-id="ef489-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef489-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef489-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef489-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef489-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef489-126">CommonParameters</span></span>
<span data-ttu-id="ef489-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ef489-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef489-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef489-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef489-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ef489-129">INPUTS</span></span>

### <span data-ttu-id="ef489-130">沒有</span><span class="sxs-lookup"><span data-stu-id="ef489-130">None</span></span>

## <span data-ttu-id="ef489-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ef489-131">OUTPUTS</span></span>

### <span data-ttu-id="ef489-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="ef489-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ef489-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ef489-133">NOTES</span></span>

## <span data-ttu-id="ef489-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef489-134">RELATED LINKS</span></span>

[<span data-ttu-id="ef489-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ef489-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="ef489-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ef489-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="ef489-137">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ef489-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


