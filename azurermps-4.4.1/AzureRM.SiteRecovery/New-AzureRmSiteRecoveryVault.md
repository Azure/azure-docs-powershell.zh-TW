---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 786e3c17ca64acf908d06b88462f44af502e36c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624130"
---
# <span data-ttu-id="d7be3-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="d7be3-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="d7be3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d7be3-102">SYNOPSIS</span></span>
<span data-ttu-id="d7be3-103">建立網站復原服務電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="d7be3-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7be3-104">句法</span><span class="sxs-lookup"><span data-stu-id="d7be3-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7be3-105">說明</span><span class="sxs-lookup"><span data-stu-id="d7be3-105">DESCRIPTION</span></span>
<span data-ttu-id="d7be3-106">**新的-AzureRmSiteRecoveryVault** Cmdlet 會建立 Azure Site Recovery 服務保存庫。</span><span class="sxs-lookup"><span data-stu-id="d7be3-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="d7be3-107">示例</span><span class="sxs-lookup"><span data-stu-id="d7be3-107">EXAMPLES</span></span>

## <span data-ttu-id="d7be3-108">參數</span><span class="sxs-lookup"><span data-stu-id="d7be3-108">PARAMETERS</span></span>

### <span data-ttu-id="d7be3-109">-位置</span><span class="sxs-lookup"><span data-stu-id="d7be3-109">-Location</span></span>
<span data-ttu-id="d7be3-110">指定地理位置名稱。</span><span class="sxs-lookup"><span data-stu-id="d7be3-110">Specifies the geographical location name.</span></span>

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

### <span data-ttu-id="d7be3-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7be3-111">-Name</span></span>
<span data-ttu-id="d7be3-112">指定保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7be3-112">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="d7be3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7be3-113">-ResourceGroupName</span></span>
<span data-ttu-id="d7be3-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7be3-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d7be3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7be3-115">-DefaultProfile</span></span>
<span data-ttu-id="d7be3-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d7be3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7be3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7be3-117">CommonParameters</span></span>
<span data-ttu-id="d7be3-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d7be3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7be3-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d7be3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7be3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="d7be3-120">INPUTS</span></span>

## <span data-ttu-id="d7be3-121">輸出</span><span class="sxs-lookup"><span data-stu-id="d7be3-121">OUTPUTS</span></span>

## <span data-ttu-id="d7be3-122">筆記</span><span class="sxs-lookup"><span data-stu-id="d7be3-122">NOTES</span></span>

## <span data-ttu-id="d7be3-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7be3-123">RELATED LINKS</span></span>

[<span data-ttu-id="d7be3-124">AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="d7be3-124">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="d7be3-125">移除-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="d7be3-125">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
