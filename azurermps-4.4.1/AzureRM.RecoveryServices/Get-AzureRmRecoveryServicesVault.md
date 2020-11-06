---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bd9b47b54cb609a06da10488007f55d91d157b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453308"
---
# <span data-ttu-id="1f05a-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="1f05a-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="1f05a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f05a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f05a-103">取得恢復服務電子倉庫的清單。</span><span class="sxs-lookup"><span data-stu-id="1f05a-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f05a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f05a-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f05a-105">說明</span><span class="sxs-lookup"><span data-stu-id="1f05a-105">DESCRIPTION</span></span>
<span data-ttu-id="1f05a-106">**AzureRmRecoveryServicesVault** Cmdlet 會在目前的訂閱中取得恢復服務電子倉庫的清單。</span><span class="sxs-lookup"><span data-stu-id="1f05a-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="1f05a-107">示例</span><span class="sxs-lookup"><span data-stu-id="1f05a-107">EXAMPLES</span></span>

## <span data-ttu-id="1f05a-108">參數</span><span class="sxs-lookup"><span data-stu-id="1f05a-108">PARAMETERS</span></span>

### <span data-ttu-id="1f05a-109">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f05a-109">-Name</span></span>
<span data-ttu-id="1f05a-110">指定要查詢之保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f05a-110">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="1f05a-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f05a-111">-ResourceGroupName</span></span>
<span data-ttu-id="1f05a-112">指定 Azure 資源群組的名稱，以在其中建立指定的復原服務物件，或從該資源群組中取得。</span><span class="sxs-lookup"><span data-stu-id="1f05a-112">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="1f05a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f05a-113">-DefaultProfile</span></span>
<span data-ttu-id="1f05a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f05a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f05a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f05a-115">CommonParameters</span></span>
<span data-ttu-id="1f05a-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f05a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f05a-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f05a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f05a-118">輸入</span><span class="sxs-lookup"><span data-stu-id="1f05a-118">INPUTS</span></span>

## <span data-ttu-id="1f05a-119">輸出</span><span class="sxs-lookup"><span data-stu-id="1f05a-119">OUTPUTS</span></span>

### <span data-ttu-id="1f05a-120">[System.object]. 清單 ' 1 [RecoveryServices. ARSVault]</span><span class="sxs-lookup"><span data-stu-id="1f05a-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="1f05a-121">筆記</span><span class="sxs-lookup"><span data-stu-id="1f05a-121">NOTES</span></span>

## <span data-ttu-id="1f05a-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f05a-122">RELATED LINKS</span></span>

[<span data-ttu-id="1f05a-123">AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1f05a-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="1f05a-124">新-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="1f05a-124">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="1f05a-125">移除-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="1f05a-125">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


