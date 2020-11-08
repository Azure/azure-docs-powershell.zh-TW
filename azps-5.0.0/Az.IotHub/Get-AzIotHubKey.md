---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139188"
---
# <span data-ttu-id="91132-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="91132-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="91132-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91132-102">SYNOPSIS</span></span>
<span data-ttu-id="91132-103">取得 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="91132-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="91132-104">句法</span><span class="sxs-lookup"><span data-stu-id="91132-104">SYNTAX</span></span>

### <span data-ttu-id="91132-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="91132-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91132-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="91132-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91132-107">說明</span><span class="sxs-lookup"><span data-stu-id="91132-107">DESCRIPTION</span></span>
<span data-ttu-id="91132-108">取得 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="91132-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="91132-109">您可以列出所有按鍵，或依據特定的索引鍵名稱來篩選清單。</span><span class="sxs-lookup"><span data-stu-id="91132-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="91132-110">示例</span><span class="sxs-lookup"><span data-stu-id="91132-110">EXAMPLES</span></span>

### <span data-ttu-id="91132-111">範例1取得所有按鍵</span><span class="sxs-lookup"><span data-stu-id="91132-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="91132-112">取得名為 "myiothub" 的 IotHub 的所有鍵</span><span class="sxs-lookup"><span data-stu-id="91132-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="91132-113">範例2取得特定金鑰的資訊</span><span class="sxs-lookup"><span data-stu-id="91132-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="91132-114">取得名為「iothubowner」的名為「myiothub」之 IotHub 的索引鍵資訊</span><span class="sxs-lookup"><span data-stu-id="91132-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="91132-115">參數</span><span class="sxs-lookup"><span data-stu-id="91132-115">PARAMETERS</span></span>

### <span data-ttu-id="91132-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91132-116">-DefaultProfile</span></span>
<span data-ttu-id="91132-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="91132-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91132-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="91132-118">-HubId</span></span>
<span data-ttu-id="91132-119">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="91132-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="91132-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="91132-120">-KeyName</span></span>
<span data-ttu-id="91132-121">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="91132-121">Name of the Key</span></span>

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

### <span data-ttu-id="91132-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="91132-122">-Name</span></span>
<span data-ttu-id="91132-123">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="91132-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="91132-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91132-124">-ResourceGroupName</span></span>
<span data-ttu-id="91132-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="91132-125">Resource Group Name</span></span>

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

### <span data-ttu-id="91132-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91132-126">CommonParameters</span></span>
<span data-ttu-id="91132-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91132-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91132-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91132-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91132-129">輸入</span><span class="sxs-lookup"><span data-stu-id="91132-129">INPUTS</span></span>

### <span data-ttu-id="91132-130">System.object</span><span class="sxs-lookup"><span data-stu-id="91132-130">System.String</span></span>

## <span data-ttu-id="91132-131">輸出</span><span class="sxs-lookup"><span data-stu-id="91132-131">OUTPUTS</span></span>

### <span data-ttu-id="91132-132">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="91132-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="91132-133">筆記</span><span class="sxs-lookup"><span data-stu-id="91132-133">NOTES</span></span>

## <span data-ttu-id="91132-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="91132-134">RELATED LINKS</span></span>
