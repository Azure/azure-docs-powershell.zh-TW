---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 6937d79d6f60c053238075713f5d58432124e7e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911101"
---
# <span data-ttu-id="9f55f-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="9f55f-101">Get-AzIotHub</span></span>

## <span data-ttu-id="9f55f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9f55f-102">SYNOPSIS</span></span>
<span data-ttu-id="9f55f-103">獲得訂閱中 IotHubs 的資訊。</span><span class="sxs-lookup"><span data-stu-id="9f55f-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="9f55f-104">語法</span><span class="sxs-lookup"><span data-stu-id="9f55f-104">SYNTAX</span></span>

### <span data-ttu-id="9f55f-105">ListIotHubsByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="9f55f-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f55f-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="9f55f-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f55f-107">描述</span><span class="sxs-lookup"><span data-stu-id="9f55f-107">DESCRIPTION</span></span>
<span data-ttu-id="9f55f-108">獲得訂閱中 IotHubs 的資訊。</span><span class="sxs-lookup"><span data-stu-id="9f55f-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="9f55f-109">您可以查看訂閱中所有的 IotHub 實例，或根據資源群組或特定的 IotHub 名稱篩選結果。</span><span class="sxs-lookup"><span data-stu-id="9f55f-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="9f55f-110">例子</span><span class="sxs-lookup"><span data-stu-id="9f55f-110">EXAMPLES</span></span>

### <span data-ttu-id="9f55f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="9f55f-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="9f55f-112">在訂閱中獲得所有 IotHub。</span><span class="sxs-lookup"><span data-stu-id="9f55f-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="9f55f-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="9f55f-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="9f55f-114">在訂閱中，獲得屬於名為"myresourcegroup"的資源組的所有 IotHub。</span><span class="sxs-lookup"><span data-stu-id="9f55f-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="9f55f-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="9f55f-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="9f55f-116">獲得名為"myiothub"的 IotHub 相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9f55f-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="9f55f-117">參數</span><span class="sxs-lookup"><span data-stu-id="9f55f-117">PARAMETERS</span></span>

### <span data-ttu-id="9f55f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f55f-118">-DefaultProfile</span></span>
<span data-ttu-id="9f55f-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="9f55f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f55f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="9f55f-120">-Name</span></span>
<span data-ttu-id="9f55f-121">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="9f55f-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="9f55f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f55f-122">-ResourceGroupName</span></span>
<span data-ttu-id="9f55f-123">ResourceGroup 的名稱</span><span class="sxs-lookup"><span data-stu-id="9f55f-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="9f55f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f55f-124">CommonParameters</span></span>
<span data-ttu-id="9f55f-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9f55f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f55f-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9f55f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f55f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9f55f-127">INPUTS</span></span>

### <span data-ttu-id="9f55f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9f55f-128">System.String</span></span>

## <span data-ttu-id="9f55f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9f55f-129">OUTPUTS</span></span>

### <span data-ttu-id="9f55f-130">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9f55f-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="9f55f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="9f55f-131">NOTES</span></span>

## <span data-ttu-id="9f55f-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f55f-132">RELATED LINKS</span></span>
