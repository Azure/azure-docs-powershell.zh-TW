---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: d544de6badaa6ce64e8165696cc7dff2a595d75e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787557"
---
# <span data-ttu-id="26e0d-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="26e0d-101">Get-AzIotHub</span></span>

## <span data-ttu-id="26e0d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="26e0d-103">取得訂閱中 IotHubs 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26e0d-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="26e0d-104">句法</span><span class="sxs-lookup"><span data-stu-id="26e0d-104">SYNTAX</span></span>

### <span data-ttu-id="26e0d-105">ListIotHubsByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="26e0d-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26e0d-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="26e0d-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26e0d-107">說明</span><span class="sxs-lookup"><span data-stu-id="26e0d-107">DESCRIPTION</span></span>
<span data-ttu-id="26e0d-108">取得訂閱中 IotHubs 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26e0d-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="26e0d-109">您可以在訂閱中查看所有 IotHub 實例，或依據資源群組或特定的 IotHub 名稱來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="26e0d-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="26e0d-110">示例</span><span class="sxs-lookup"><span data-stu-id="26e0d-110">EXAMPLES</span></span>

### <span data-ttu-id="26e0d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="26e0d-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="26e0d-112">取得訂閱中的所有 IotHubs。</span><span class="sxs-lookup"><span data-stu-id="26e0d-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="26e0d-113">範例2</span><span class="sxs-lookup"><span data-stu-id="26e0d-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="26e0d-114">取得訂閱中名為 "myresourcegroup" 的資源 IotHubs 中的所有。</span><span class="sxs-lookup"><span data-stu-id="26e0d-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="26e0d-115">範例3</span><span class="sxs-lookup"><span data-stu-id="26e0d-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="26e0d-116">取得名為 "myiothub" 的 IotHub 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26e0d-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="26e0d-117">參數</span><span class="sxs-lookup"><span data-stu-id="26e0d-117">PARAMETERS</span></span>

### <span data-ttu-id="26e0d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e0d-118">-DefaultProfile</span></span>
<span data-ttu-id="26e0d-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="26e0d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26e0d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="26e0d-120">-Name</span></span>
<span data-ttu-id="26e0d-121">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="26e0d-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="26e0d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e0d-122">-ResourceGroupName</span></span>
<span data-ttu-id="26e0d-123">ResourceGroup 的名稱</span><span class="sxs-lookup"><span data-stu-id="26e0d-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="26e0d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e0d-124">CommonParameters</span></span>
<span data-ttu-id="26e0d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26e0d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e0d-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26e0d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e0d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="26e0d-127">INPUTS</span></span>

### <span data-ttu-id="26e0d-128">System.object</span><span class="sxs-lookup"><span data-stu-id="26e0d-128">System.String</span></span>

## <span data-ttu-id="26e0d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="26e0d-129">OUTPUTS</span></span>

### <span data-ttu-id="26e0d-130">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="26e0d-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="26e0d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="26e0d-131">NOTES</span></span>

## <span data-ttu-id="26e0d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="26e0d-132">RELATED LINKS</span></span>
