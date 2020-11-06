---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 44cb5e9317c1806200a571dd6311e212e50a8c20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448406"
---
# <span data-ttu-id="e62df-101">Get-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="e62df-101">Get-AzureRmIotHub</span></span>

## <span data-ttu-id="e62df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e62df-102">SYNOPSIS</span></span>
<span data-ttu-id="e62df-103">取得訂閱中 IotHubs 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e62df-103">Gets information about the IotHubs in a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e62df-104">句法</span><span class="sxs-lookup"><span data-stu-id="e62df-104">SYNTAX</span></span>

### <span data-ttu-id="e62df-105">ListIotHubsByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="e62df-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e62df-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="e62df-106">GetIotHubByName</span></span>
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e62df-107">說明</span><span class="sxs-lookup"><span data-stu-id="e62df-107">DESCRIPTION</span></span>
<span data-ttu-id="e62df-108">取得訂閱中 IotHubs 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e62df-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="e62df-109">您可以在訂閱中查看所有 IotHub 實例，或依據資源群組或特定的 IotHub 名稱來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="e62df-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="e62df-110">示例</span><span class="sxs-lookup"><span data-stu-id="e62df-110">EXAMPLES</span></span>

### <span data-ttu-id="e62df-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e62df-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHub
```

<span data-ttu-id="e62df-112">取得訂閱中的所有 IotHubs。</span><span class="sxs-lookup"><span data-stu-id="e62df-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="e62df-113">範例2</span><span class="sxs-lookup"><span data-stu-id="e62df-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="e62df-114">取得訂閱中名為 "myresourcegroup" 的資源 IotHubs 中的所有。</span><span class="sxs-lookup"><span data-stu-id="e62df-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="e62df-115">範例3</span><span class="sxs-lookup"><span data-stu-id="e62df-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e62df-116">取得名為 "myiothub" 的 IotHub 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e62df-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="e62df-117">參數</span><span class="sxs-lookup"><span data-stu-id="e62df-117">PARAMETERS</span></span>

### <span data-ttu-id="e62df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62df-118">-DefaultProfile</span></span>
<span data-ttu-id="e62df-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e62df-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e62df-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e62df-120">-Name</span></span>
<span data-ttu-id="e62df-121">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="e62df-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e62df-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e62df-122">-ResourceGroupName</span></span>
<span data-ttu-id="e62df-123">ResourceGroup 的名稱</span><span class="sxs-lookup"><span data-stu-id="e62df-123">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e62df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62df-124">CommonParameters</span></span>
<span data-ttu-id="e62df-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e62df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62df-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e62df-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62df-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e62df-127">INPUTS</span></span>

### <span data-ttu-id="e62df-128">System.object</span><span class="sxs-lookup"><span data-stu-id="e62df-128">System.String</span></span>

## <span data-ttu-id="e62df-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e62df-129">OUTPUTS</span></span>

### <span data-ttu-id="e62df-130">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="e62df-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="e62df-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e62df-131">NOTES</span></span>

## <span data-ttu-id="e62df-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e62df-132">RELATED LINKS</span></span>
