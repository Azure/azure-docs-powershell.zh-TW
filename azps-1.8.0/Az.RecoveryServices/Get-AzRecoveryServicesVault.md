---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: 5dfe76ad08c59a661d6907c65a53da9397f0a66d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621127"
---
# <span data-ttu-id="ddc87-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ddc87-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="ddc87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ddc87-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc87-103">取得恢復服務電子倉庫的清單。</span><span class="sxs-lookup"><span data-stu-id="ddc87-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="ddc87-104">句法</span><span class="sxs-lookup"><span data-stu-id="ddc87-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddc87-105">說明</span><span class="sxs-lookup"><span data-stu-id="ddc87-105">DESCRIPTION</span></span>
<span data-ttu-id="ddc87-106">**AzRecoveryServicesVault** Cmdlet 會在目前的訂閱中取得恢復服務電子倉庫的清單。</span><span class="sxs-lookup"><span data-stu-id="ddc87-106">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="ddc87-107">示例</span><span class="sxs-lookup"><span data-stu-id="ddc87-107">EXAMPLES</span></span>

### <span data-ttu-id="ddc87-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ddc87-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="ddc87-109">在選取的訂閱中取得保存庫清單。</span><span class="sxs-lookup"><span data-stu-id="ddc87-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="ddc87-110">範例2</span><span class="sxs-lookup"><span data-stu-id="ddc87-110">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="ddc87-111">在 [資源群組] 中取得選取訂閱的電子倉庫清單。</span><span class="sxs-lookup"><span data-stu-id="ddc87-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="ddc87-112">範例3</span><span class="sxs-lookup"><span data-stu-id="ddc87-112">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="ddc87-113">在資源群組中取得具有指定名稱的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="ddc87-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="ddc87-114">參數</span><span class="sxs-lookup"><span data-stu-id="ddc87-114">PARAMETERS</span></span>

### <span data-ttu-id="ddc87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc87-115">-DefaultProfile</span></span>
<span data-ttu-id="ddc87-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ddc87-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddc87-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ddc87-117">-Name</span></span>
<span data-ttu-id="ddc87-118">指定要查詢之保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddc87-118">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc87-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc87-119">-ResourceGroupName</span></span>
<span data-ttu-id="ddc87-120">指定 Azure 資源群組的名稱，以在其中建立指定的復原服務物件，或從該資源群組中取得。</span><span class="sxs-lookup"><span data-stu-id="ddc87-120">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc87-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc87-121">CommonParameters</span></span>
<span data-ttu-id="ddc87-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ddc87-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc87-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ddc87-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc87-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ddc87-124">INPUTS</span></span>

### <span data-ttu-id="ddc87-125">所有</span><span class="sxs-lookup"><span data-stu-id="ddc87-125">None</span></span>

## <span data-ttu-id="ddc87-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ddc87-126">OUTPUTS</span></span>

### <span data-ttu-id="ddc87-127">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ddc87-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ddc87-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ddc87-128">NOTES</span></span>

## <span data-ttu-id="ddc87-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddc87-129">RELATED LINKS</span></span>

[<span data-ttu-id="ddc87-130">AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ddc87-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="ddc87-131">新-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ddc87-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="ddc87-132">移除-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ddc87-132">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


