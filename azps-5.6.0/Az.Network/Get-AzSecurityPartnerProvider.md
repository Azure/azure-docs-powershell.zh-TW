---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 99498979df259723a192bd0e2fd74ef436ae0ee1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902433"
---
# <span data-ttu-id="f019b-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f019b-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="f019b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f019b-102">SYNOPSIS</span></span>
<span data-ttu-id="f019b-103">取得 Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f019b-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="f019b-104">語法</span><span class="sxs-lookup"><span data-stu-id="f019b-104">SYNTAX</span></span>

### <span data-ttu-id="f019b-105">SecurityPartnerProviderNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f019b-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f019b-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f019b-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f019b-107">描述</span><span class="sxs-lookup"><span data-stu-id="f019b-107">DESCRIPTION</span></span>
<span data-ttu-id="f019b-108">**Get-AzSecurityPartnerProvider Cmdlet** 取得 Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f019b-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="f019b-109">例子</span><span class="sxs-lookup"><span data-stu-id="f019b-109">EXAMPLES</span></span>

### <span data-ttu-id="f019b-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="f019b-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="f019b-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="f019b-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="f019b-112">參數</span><span class="sxs-lookup"><span data-stu-id="f019b-112">PARAMETERS</span></span>

### <span data-ttu-id="f019b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f019b-113">-DefaultProfile</span></span>
<span data-ttu-id="f019b-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f019b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f019b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f019b-115">-Name</span></span>
<span data-ttu-id="f019b-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f019b-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f019b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f019b-117">-ResourceGroupName</span></span>
<span data-ttu-id="f019b-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f019b-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f019b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f019b-119">-ResourceId</span></span>
<span data-ttu-id="f019b-120">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f019b-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f019b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f019b-121">CommonParameters</span></span>
<span data-ttu-id="f019b-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f019b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f019b-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f019b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f019b-124">輸入</span><span class="sxs-lookup"><span data-stu-id="f019b-124">INPUTS</span></span>

### <span data-ttu-id="f019b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f019b-125">System.String</span></span>

## <span data-ttu-id="f019b-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f019b-126">OUTPUTS</span></span>

### <span data-ttu-id="f019b-127">Microsoft.Azure.Commands.Network.models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f019b-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="f019b-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f019b-128">NOTES</span></span>

## <span data-ttu-id="f019b-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f019b-129">RELATED LINKS</span></span>
