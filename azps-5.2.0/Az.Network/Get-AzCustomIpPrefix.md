---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98272968"
---
# <span data-ttu-id="edae0-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="edae0-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="edae0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="edae0-102">SYNOPSIS</span></span>
<span data-ttu-id="edae0-103">取得 CustomIpPrefix 資源</span><span class="sxs-lookup"><span data-stu-id="edae0-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="edae0-104">句法</span><span class="sxs-lookup"><span data-stu-id="edae0-104">SYNTAX</span></span>

### <span data-ttu-id="edae0-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="edae0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="edae0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="edae0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edae0-107">說明</span><span class="sxs-lookup"><span data-stu-id="edae0-107">DESCRIPTION</span></span>
<span data-ttu-id="edae0-108">**AzCustomIpPrefix** Cmdlet 會取得一或多個已知輸入參數集的 CustomIpPrefixes</span><span class="sxs-lookup"><span data-stu-id="edae0-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="edae0-109">示例</span><span class="sxs-lookup"><span data-stu-id="edae0-109">EXAMPLES</span></span>

### <span data-ttu-id="edae0-110">範例1</span><span class="sxs-lookup"><span data-stu-id="edae0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myCustomIpPrefix

Name                 : myCustomIpPrefix
ResourceGroupName    : myRg
Location             : westus
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/byoip-test-rg/providers/Micro
                       soft.Network/customIPPrefixes/testCustomIpPrefix
Etag                 : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid         : 00000000-0000-0000-0000-000000000000
ProvisioningState    : Succeeded
Tags                 :
Cidr                 : 111.111.111.111/24
CommissionedState    : Provisioning
PublicIpPrefixes     : []
Zones                : {}
```

<span data-ttu-id="edae0-111">這個命令會在資源群組 myRg 中取得名為 myCustomIpPrefix 的 CustomIpPrefix 資源。</span><span class="sxs-lookup"><span data-stu-id="edae0-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="edae0-112">參數</span><span class="sxs-lookup"><span data-stu-id="edae0-112">PARAMETERS</span></span>

### <span data-ttu-id="edae0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edae0-113">-DefaultProfile</span></span>
<span data-ttu-id="edae0-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="edae0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edae0-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="edae0-115">-Name</span></span>
<span data-ttu-id="edae0-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="edae0-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edae0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edae0-117">-ResourceGroupName</span></span>
<span data-ttu-id="edae0-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="edae0-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edae0-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edae0-119">-ResourceId</span></span>
<span data-ttu-id="edae0-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="edae0-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edae0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edae0-121">CommonParameters</span></span>
<span data-ttu-id="edae0-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="edae0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edae0-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="edae0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edae0-124">輸入</span><span class="sxs-lookup"><span data-stu-id="edae0-124">INPUTS</span></span>

### <span data-ttu-id="edae0-125">System.object</span><span class="sxs-lookup"><span data-stu-id="edae0-125">System.String</span></span>

## <span data-ttu-id="edae0-126">輸出</span><span class="sxs-lookup"><span data-stu-id="edae0-126">OUTPUTS</span></span>

### <span data-ttu-id="edae0-127">PSCustomIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="edae0-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="edae0-128">筆記</span><span class="sxs-lookup"><span data-stu-id="edae0-128">NOTES</span></span>

## <span data-ttu-id="edae0-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="edae0-129">RELATED LINKS</span></span>

[<span data-ttu-id="edae0-130">新-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="edae0-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="edae0-131">移除-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="edae0-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="edae0-132">更新-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="edae0-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)