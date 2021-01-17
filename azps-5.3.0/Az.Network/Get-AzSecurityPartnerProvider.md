---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449342"
---
# <span data-ttu-id="1d252-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1d252-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="1d252-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d252-102">SYNOPSIS</span></span>
<span data-ttu-id="1d252-103">取得 Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1d252-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="1d252-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d252-104">SYNTAX</span></span>

### <span data-ttu-id="1d252-105">SecurityPartnerProviderNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1d252-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d252-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d252-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d252-107">說明</span><span class="sxs-lookup"><span data-stu-id="1d252-107">DESCRIPTION</span></span>
<span data-ttu-id="1d252-108">**AzSecurityPartnerProvider** Cmdlet 會取得 Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1d252-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="1d252-109">示例</span><span class="sxs-lookup"><span data-stu-id="1d252-109">EXAMPLES</span></span>

### <span data-ttu-id="1d252-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1d252-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="1d252-111">範例2</span><span class="sxs-lookup"><span data-stu-id="1d252-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="1d252-112">參數</span><span class="sxs-lookup"><span data-stu-id="1d252-112">PARAMETERS</span></span>

### <span data-ttu-id="1d252-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d252-113">-DefaultProfile</span></span>
<span data-ttu-id="1d252-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d252-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d252-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1d252-115">-Name</span></span>
<span data-ttu-id="1d252-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="1d252-116">The resource name.</span></span>

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

### <span data-ttu-id="1d252-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d252-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d252-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d252-118">The resource group name.</span></span>

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

### <span data-ttu-id="1d252-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d252-119">-ResourceId</span></span>
<span data-ttu-id="1d252-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="1d252-120">The resource Id.</span></span>

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

### <span data-ttu-id="1d252-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d252-121">CommonParameters</span></span>
<span data-ttu-id="1d252-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d252-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d252-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1d252-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d252-124">輸入</span><span class="sxs-lookup"><span data-stu-id="1d252-124">INPUTS</span></span>

### <span data-ttu-id="1d252-125">System.object</span><span class="sxs-lookup"><span data-stu-id="1d252-125">System.String</span></span>

## <span data-ttu-id="1d252-126">輸出</span><span class="sxs-lookup"><span data-stu-id="1d252-126">OUTPUTS</span></span>

### <span data-ttu-id="1d252-127">PSSecurityPartnerProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1d252-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="1d252-128">筆記</span><span class="sxs-lookup"><span data-stu-id="1d252-128">NOTES</span></span>

## <span data-ttu-id="1d252-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d252-129">RELATED LINKS</span></span>
