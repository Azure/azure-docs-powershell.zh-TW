---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bbc059751ee4713b59f6b915efe32bdf57419be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453104"
---
# <span data-ttu-id="040e7-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="040e7-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="040e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="040e7-102">SYNOPSIS</span></span>
<span data-ttu-id="040e7-103">取得恢復服務電子倉庫的清單。</span><span class="sxs-lookup"><span data-stu-id="040e7-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="040e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="040e7-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="040e7-105">說明</span><span class="sxs-lookup"><span data-stu-id="040e7-105">DESCRIPTION</span></span>
<span data-ttu-id="040e7-106">**AzureRmRecoveryServicesVault** Cmdlet 會在目前的訂閱中取得恢復服務電子倉庫的清單。</span><span class="sxs-lookup"><span data-stu-id="040e7-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="040e7-107">示例</span><span class="sxs-lookup"><span data-stu-id="040e7-107">EXAMPLES</span></span>

### <span data-ttu-id="040e7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="040e7-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault
```

<span data-ttu-id="040e7-109">在選取的訂閱中取得保存庫清單。</span><span class="sxs-lookup"><span data-stu-id="040e7-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="040e7-110">範例2</span><span class="sxs-lookup"><span data-stu-id="040e7-110">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="040e7-111">在 [資源群組] 中取得選取訂閱的電子倉庫清單。</span><span class="sxs-lookup"><span data-stu-id="040e7-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="040e7-112">範例3</span><span class="sxs-lookup"><span data-stu-id="040e7-112">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="040e7-113">在資源群組中取得具有指定名稱的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="040e7-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="040e7-114">參數</span><span class="sxs-lookup"><span data-stu-id="040e7-114">PARAMETERS</span></span>

### <span data-ttu-id="040e7-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="040e7-115">-Name</span></span>
<span data-ttu-id="040e7-116">指定要查詢之保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="040e7-116">Specifies the name of the vault to query for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="040e7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="040e7-117">-ResourceGroupName</span></span>
<span data-ttu-id="040e7-118">指定 Azure 資源群組的名稱，以在其中建立指定的復原服務物件，或從該資源群組中取得。</span><span class="sxs-lookup"><span data-stu-id="040e7-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="040e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="040e7-119">-DefaultProfile</span></span>
<span data-ttu-id="040e7-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="040e7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="040e7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="040e7-121">CommonParameters</span></span>
<span data-ttu-id="040e7-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="040e7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="040e7-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="040e7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="040e7-124">輸入</span><span class="sxs-lookup"><span data-stu-id="040e7-124">INPUTS</span></span>

### <span data-ttu-id="040e7-125">所有</span><span class="sxs-lookup"><span data-stu-id="040e7-125">None</span></span>
<span data-ttu-id="040e7-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="040e7-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="040e7-127">輸出</span><span class="sxs-lookup"><span data-stu-id="040e7-127">OUTPUTS</span></span>

### <span data-ttu-id="040e7-128">[System.object]. 清單 ' 1 [RecoveryServices. ARSVault]</span><span class="sxs-lookup"><span data-stu-id="040e7-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="040e7-129">筆記</span><span class="sxs-lookup"><span data-stu-id="040e7-129">NOTES</span></span>

## <span data-ttu-id="040e7-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="040e7-130">RELATED LINKS</span></span>

[<span data-ttu-id="040e7-131">AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="040e7-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="040e7-132">新-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="040e7-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="040e7-133">移除-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="040e7-133">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


