---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: 8ef418202025e7525dd5da74219501f11e69a5a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903501"
---
# <span data-ttu-id="2ae87-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="2ae87-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="2ae87-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2ae87-102">SYNOPSIS</span></span>
<span data-ttu-id="2ae87-103">建立私人 DNS 區域群組的 DNS 區域組。</span><span class="sxs-lookup"><span data-stu-id="2ae87-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="2ae87-104">語法</span><span class="sxs-lookup"><span data-stu-id="2ae87-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ae87-105">描述</span><span class="sxs-lookup"><span data-stu-id="2ae87-105">DESCRIPTION</span></span>
<span data-ttu-id="2ae87-106">**New-AzPrivateDnsZoneConfig** Cmdlet 可讓您建立一個新的 DNS 區域設定物件，物件會設定在 DNS 區域群組上。</span><span class="sxs-lookup"><span data-stu-id="2ae87-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="2ae87-107">例子</span><span class="sxs-lookup"><span data-stu-id="2ae87-107">EXAMPLES</span></span>

### <span data-ttu-id="2ae87-108">建立 DNS 區域組</span><span class="sxs-lookup"><span data-stu-id="2ae87-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="2ae87-109">上述範例會建立 DNS 區域，然後建立 DNS 區域組配置。</span><span class="sxs-lookup"><span data-stu-id="2ae87-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="2ae87-110">`New-AzPrivateDnsZone` 模組 Az.PrivateDns 已驗證 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ae87-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="2ae87-111">參數</span><span class="sxs-lookup"><span data-stu-id="2ae87-111">PARAMETERS</span></span>

### <span data-ttu-id="2ae87-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ae87-112">-DefaultProfile</span></span>
<span data-ttu-id="2ae87-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ae87-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ae87-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ae87-114">-Name</span></span>
<span data-ttu-id="2ae87-115">資源群組中唯一資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ae87-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="2ae87-116">這個名稱可以用來存取資源。</span><span class="sxs-lookup"><span data-stu-id="2ae87-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="2ae87-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="2ae87-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="2ae87-118">私人 dns 區域的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ae87-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="2ae87-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ae87-119">CommonParameters</span></span>
<span data-ttu-id="2ae87-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2ae87-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ae87-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ae87-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ae87-122">輸入</span><span class="sxs-lookup"><span data-stu-id="2ae87-122">INPUTS</span></span>

### <span data-ttu-id="2ae87-123">沒有</span><span class="sxs-lookup"><span data-stu-id="2ae87-123">None</span></span>

## <span data-ttu-id="2ae87-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2ae87-124">OUTPUTS</span></span>

### <span data-ttu-id="2ae87-125">Microsoft.Azure.Commands.Network.models.PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="2ae87-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="2ae87-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2ae87-126">NOTES</span></span>

## <span data-ttu-id="2ae87-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ae87-127">RELATED LINKS</span></span>
