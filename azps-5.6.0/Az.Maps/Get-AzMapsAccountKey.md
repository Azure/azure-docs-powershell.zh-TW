---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: bce5110a4aa03686b8ae38ee03ea853bc6c89949
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912822"
---
# <span data-ttu-id="0db18-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="0db18-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="0db18-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0db18-102">SYNOPSIS</span></span>
<span data-ttu-id="0db18-103">獲得帳戶的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="0db18-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="0db18-104">這些金鑰是後續 Azure 地圖服務通話中使用的驗證機制。</span><span class="sxs-lookup"><span data-stu-id="0db18-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="0db18-105">語法</span><span class="sxs-lookup"><span data-stu-id="0db18-105">SYNTAX</span></span>

### <span data-ttu-id="0db18-106">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0db18-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0db18-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0db18-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0db18-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0db18-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0db18-109">描述</span><span class="sxs-lookup"><span data-stu-id="0db18-109">DESCRIPTION</span></span>
<span data-ttu-id="0db18-110">Cmdlet Get-AzMapsAccountKey提供 Azure 地圖服務帳戶的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="0db18-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="0db18-111">Azure 地圖帳戶有兩個 API 金鑰：主要和次要。</span><span class="sxs-lookup"><span data-stu-id="0db18-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="0db18-112">這些按鍵可啟用與 Azure 地圖服務帳戶端點的互動。</span><span class="sxs-lookup"><span data-stu-id="0db18-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="0db18-113">使用New-AzMapsAccountKey (New-AzMapsAccountKey.md) 重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="0db18-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="0db18-114">例子</span><span class="sxs-lookup"><span data-stu-id="0db18-114">EXAMPLES</span></span>

### <span data-ttu-id="0db18-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="0db18-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="0db18-116">會針對資源群組 MyResourceGroup 中名為 MyAccount 的帳戶，返回金鑰。</span><span class="sxs-lookup"><span data-stu-id="0db18-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="0db18-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="0db18-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="0db18-118">會針對指定的 Azure 地圖服務帳戶，返回金鑰。</span><span class="sxs-lookup"><span data-stu-id="0db18-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="0db18-119">參數</span><span class="sxs-lookup"><span data-stu-id="0db18-119">PARAMETERS</span></span>

### <span data-ttu-id="0db18-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db18-120">-DefaultProfile</span></span>
<span data-ttu-id="0db18-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0db18-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0db18-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0db18-122">-InputObject</span></span>
<span data-ttu-id="0db18-123">從 Get-AzMapsAccount移來的地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="0db18-123">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0db18-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="0db18-124">-Name</span></span>
<span data-ttu-id="0db18-125">地圖帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0db18-125">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db18-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db18-126">-ResourceGroupName</span></span>
<span data-ttu-id="0db18-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0db18-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db18-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0db18-128">-ResourceId</span></span>
<span data-ttu-id="0db18-129">地圖帳戶 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="0db18-129">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db18-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db18-130">CommonParameters</span></span>
<span data-ttu-id="0db18-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0db18-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db18-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0db18-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db18-133">輸入</span><span class="sxs-lookup"><span data-stu-id="0db18-133">INPUTS</span></span>

### <span data-ttu-id="0db18-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0db18-134">System.String</span></span>

### <span data-ttu-id="0db18-135">Microsoft.Azure.Commands.Maps.models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="0db18-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="0db18-136">輸出</span><span class="sxs-lookup"><span data-stu-id="0db18-136">OUTPUTS</span></span>

### <span data-ttu-id="0db18-137">Microsoft.Azure.Commands.Maps.models.PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0db18-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="0db18-138">筆記</span><span class="sxs-lookup"><span data-stu-id="0db18-138">NOTES</span></span>

## <span data-ttu-id="0db18-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="0db18-139">RELATED LINKS</span></span>
