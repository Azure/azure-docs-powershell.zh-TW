---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283764"
---
# <span data-ttu-id="b8346-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="b8346-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="b8346-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8346-102">SYNOPSIS</span></span>
<span data-ttu-id="b8346-103">建立 [私人 DNS 區域] 群組的 DNS 區域設定。</span><span class="sxs-lookup"><span data-stu-id="b8346-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="b8346-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8346-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8346-105">說明</span><span class="sxs-lookup"><span data-stu-id="b8346-105">DESCRIPTION</span></span>
<span data-ttu-id="b8346-106">**新的-AzPrivateDnsZoneConfig** Cmdlet 可讓您建立新的 dns 區域設定物件，該物件將會在 DNS 區域群組上設定。</span><span class="sxs-lookup"><span data-stu-id="b8346-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="b8346-107">示例</span><span class="sxs-lookup"><span data-stu-id="b8346-107">EXAMPLES</span></span>

### <span data-ttu-id="b8346-108">建立 DNS 區域設定</span><span class="sxs-lookup"><span data-stu-id="b8346-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="b8346-109">上述範例會建立 DNS 區域，然後建立 DNS 區域設定。</span><span class="sxs-lookup"><span data-stu-id="b8346-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="b8346-110">`New-AzPrivateDnsZone` proveded 是由 module Az PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="b8346-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="b8346-111">參數</span><span class="sxs-lookup"><span data-stu-id="b8346-111">PARAMETERS</span></span>

### <span data-ttu-id="b8346-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8346-112">-DefaultProfile</span></span>
<span data-ttu-id="b8346-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8346-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8346-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8346-114">-Name</span></span>
<span data-ttu-id="b8346-115">資源群組中唯一的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b8346-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="b8346-116">此名稱可以用來存取資源。</span><span class="sxs-lookup"><span data-stu-id="b8346-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="b8346-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="b8346-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="b8346-118">私人 dns 區域的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8346-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="b8346-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8346-119">CommonParameters</span></span>
<span data-ttu-id="b8346-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8346-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8346-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b8346-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8346-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b8346-122">INPUTS</span></span>

### <span data-ttu-id="b8346-123">所有</span><span class="sxs-lookup"><span data-stu-id="b8346-123">None</span></span>

## <span data-ttu-id="b8346-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b8346-124">OUTPUTS</span></span>

### <span data-ttu-id="b8346-125">PSPrivateDnsZoneConfig 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b8346-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="b8346-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b8346-126">NOTES</span></span>

## <span data-ttu-id="b8346-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8346-127">RELATED LINKS</span></span>
