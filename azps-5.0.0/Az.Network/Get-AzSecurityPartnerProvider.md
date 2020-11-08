---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141136"
---
# <span data-ttu-id="16e73-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="16e73-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="16e73-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16e73-102">SYNOPSIS</span></span>
<span data-ttu-id="16e73-103">取得 Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="16e73-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="16e73-104">句法</span><span class="sxs-lookup"><span data-stu-id="16e73-104">SYNTAX</span></span>

### <span data-ttu-id="16e73-105">SecurityPartnerProviderNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="16e73-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16e73-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16e73-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16e73-107">說明</span><span class="sxs-lookup"><span data-stu-id="16e73-107">DESCRIPTION</span></span>
<span data-ttu-id="16e73-108">**AzSecurityPartnerProvider** Cmdlet 會取得 Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="16e73-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="16e73-109">示例</span><span class="sxs-lookup"><span data-stu-id="16e73-109">EXAMPLES</span></span>

### <span data-ttu-id="16e73-110">範例1</span><span class="sxs-lookup"><span data-stu-id="16e73-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="16e73-111">範例2</span><span class="sxs-lookup"><span data-stu-id="16e73-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="16e73-112">參數</span><span class="sxs-lookup"><span data-stu-id="16e73-112">PARAMETERS</span></span>

### <span data-ttu-id="16e73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e73-113">-DefaultProfile</span></span>
<span data-ttu-id="16e73-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16e73-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16e73-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="16e73-115">-Name</span></span>
<span data-ttu-id="16e73-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="16e73-116">The resource name.</span></span>

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

### <span data-ttu-id="16e73-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e73-117">-ResourceGroupName</span></span>
<span data-ttu-id="16e73-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="16e73-118">The resource group name.</span></span>

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

### <span data-ttu-id="16e73-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16e73-119">-ResourceId</span></span>
<span data-ttu-id="16e73-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="16e73-120">The resource Id.</span></span>

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

### <span data-ttu-id="16e73-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e73-121">CommonParameters</span></span>
<span data-ttu-id="16e73-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16e73-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e73-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="16e73-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e73-124">輸入</span><span class="sxs-lookup"><span data-stu-id="16e73-124">INPUTS</span></span>

### <span data-ttu-id="16e73-125">System.object</span><span class="sxs-lookup"><span data-stu-id="16e73-125">System.String</span></span>

## <span data-ttu-id="16e73-126">輸出</span><span class="sxs-lookup"><span data-stu-id="16e73-126">OUTPUTS</span></span>

### <span data-ttu-id="16e73-127">PSSecurityPartnerProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="16e73-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="16e73-128">筆記</span><span class="sxs-lookup"><span data-stu-id="16e73-128">NOTES</span></span>

## <span data-ttu-id="16e73-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="16e73-129">RELATED LINKS</span></span>
