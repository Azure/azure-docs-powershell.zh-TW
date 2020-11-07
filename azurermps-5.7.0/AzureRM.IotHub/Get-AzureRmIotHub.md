---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 80b629fe3d5ff5e028b73b22af95243849ecede7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624088"
---
# <span data-ttu-id="ff1dc-101">Get-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="ff1dc-101">Get-AzureRmIotHub</span></span>

## <span data-ttu-id="ff1dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ff1dc-103">取得訂閱中 IotHubs 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ff1dc-103">Gets information about the IotHubs in a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff1dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff1dc-104">SYNTAX</span></span>

### <span data-ttu-id="ff1dc-105">ListIotHubsByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="ff1dc-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff1dc-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="ff1dc-106">GetIotHubByName</span></span>
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff1dc-107">說明</span><span class="sxs-lookup"><span data-stu-id="ff1dc-107">DESCRIPTION</span></span>
<span data-ttu-id="ff1dc-108">取得訂閱中 IotHubs 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ff1dc-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="ff1dc-109">您可以在訂閱中查看所有 IotHub 實例，或依據資源群組或特定的 IotHub 名稱來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="ff1dc-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="ff1dc-110">示例</span><span class="sxs-lookup"><span data-stu-id="ff1dc-110">EXAMPLES</span></span>

### <span data-ttu-id="ff1dc-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ff1dc-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHub
```

<span data-ttu-id="ff1dc-112">取得訂閱中的所有 IotHubs。</span><span class="sxs-lookup"><span data-stu-id="ff1dc-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="ff1dc-113">範例2</span><span class="sxs-lookup"><span data-stu-id="ff1dc-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="ff1dc-114">取得訂閱中名為 "myresourcegroup" 的資源 IotHubs 中的所有。</span><span class="sxs-lookup"><span data-stu-id="ff1dc-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="ff1dc-115">範例3</span><span class="sxs-lookup"><span data-stu-id="ff1dc-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ff1dc-116">取得名為 "myiothub" 的 IotHub 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ff1dc-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="ff1dc-117">參數</span><span class="sxs-lookup"><span data-stu-id="ff1dc-117">PARAMETERS</span></span>

### <span data-ttu-id="ff1dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff1dc-118">-DefaultProfile</span></span>
<span data-ttu-id="ff1dc-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ff1dc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff1dc-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff1dc-120">-Name</span></span>
<span data-ttu-id="ff1dc-121">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="ff1dc-121">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff1dc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff1dc-122">-ResourceGroupName</span></span>
<span data-ttu-id="ff1dc-123">ResourceGroup 的名稱</span><span class="sxs-lookup"><span data-stu-id="ff1dc-123">Name of the ResourceGroup</span></span>

```yaml
Type: String
Parameter Sets: ListIotHubsByResourceGroup
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff1dc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff1dc-124">CommonParameters</span></span>
<span data-ttu-id="ff1dc-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff1dc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff1dc-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ff1dc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff1dc-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ff1dc-127">INPUTS</span></span>

### <span data-ttu-id="ff1dc-128">System.object</span><span class="sxs-lookup"><span data-stu-id="ff1dc-128">System.String</span></span>

## <span data-ttu-id="ff1dc-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ff1dc-129">OUTPUTS</span></span>

### <span data-ttu-id="ff1dc-130">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="ff1dc-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="ff1dc-131">\` \[ \[ PSIotHub、IotHub = 1.0.0.0、Culture = 中性、PublicKeyToken = null、Culture = 中立、版本 = 1.0.0.0、Culture = 中性、PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="ff1dc-131">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="ff1dc-132">筆記</span><span class="sxs-lookup"><span data-stu-id="ff1dc-132">NOTES</span></span>

## <span data-ttu-id="ff1dc-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff1dc-133">RELATED LINKS</span></span>

