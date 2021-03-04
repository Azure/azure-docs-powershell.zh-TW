---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 4a63f13e567a5f53726058c831107ce43768c0f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911045"
---
# <span data-ttu-id="79f36-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="79f36-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="79f36-102">簡介</span><span class="sxs-lookup"><span data-stu-id="79f36-102">SYNOPSIS</span></span>
<span data-ttu-id="79f36-103">獲得 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="79f36-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="79f36-104">語法</span><span class="sxs-lookup"><span data-stu-id="79f36-104">SYNTAX</span></span>

### <span data-ttu-id="79f36-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="79f36-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79f36-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="79f36-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79f36-107">描述</span><span class="sxs-lookup"><span data-stu-id="79f36-107">DESCRIPTION</span></span>
<span data-ttu-id="79f36-108">獲得 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="79f36-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="79f36-109">您可以列出所有 Key，或根據特定的 Key Name 篩選清單。</span><span class="sxs-lookup"><span data-stu-id="79f36-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="79f36-110">例子</span><span class="sxs-lookup"><span data-stu-id="79f36-110">EXAMPLES</span></span>

### <span data-ttu-id="79f36-111">範例 1 取得所有金鑰</span><span class="sxs-lookup"><span data-stu-id="79f36-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="79f36-112">為名為"myiothub" 的 IotHub 獲得所有金鑰</span><span class="sxs-lookup"><span data-stu-id="79f36-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="79f36-113">範例 2 取得特定金鑰的資訊</span><span class="sxs-lookup"><span data-stu-id="79f36-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="79f36-114">針對名為"myiothub" 的 IotHub，獲得名稱為 "iothubowner" 的金鑰資訊</span><span class="sxs-lookup"><span data-stu-id="79f36-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="79f36-115">參數</span><span class="sxs-lookup"><span data-stu-id="79f36-115">PARAMETERS</span></span>

### <span data-ttu-id="79f36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f36-116">-DefaultProfile</span></span>
<span data-ttu-id="79f36-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="79f36-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79f36-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="79f36-118">-HubId</span></span>
<span data-ttu-id="79f36-119">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="79f36-119">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79f36-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="79f36-120">-KeyName</span></span>
<span data-ttu-id="79f36-121">金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="79f36-121">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f36-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="79f36-122">-Name</span></span>
<span data-ttu-id="79f36-123">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="79f36-123">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79f36-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79f36-124">-ResourceGroupName</span></span>
<span data-ttu-id="79f36-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="79f36-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79f36-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f36-126">CommonParameters</span></span>
<span data-ttu-id="79f36-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="79f36-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f36-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="79f36-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f36-129">輸入</span><span class="sxs-lookup"><span data-stu-id="79f36-129">INPUTS</span></span>

### <span data-ttu-id="79f36-130">System.String</span><span class="sxs-lookup"><span data-stu-id="79f36-130">System.String</span></span>

## <span data-ttu-id="79f36-131">輸出</span><span class="sxs-lookup"><span data-stu-id="79f36-131">OUTPUTS</span></span>

### <span data-ttu-id="79f36-132">Microsoft.Azure.Commands.management.IotHub.models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="79f36-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="79f36-133">筆記</span><span class="sxs-lookup"><span data-stu-id="79f36-133">NOTES</span></span>

## <span data-ttu-id="79f36-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="79f36-134">RELATED LINKS</span></span>
