---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: c38965a99dfc152f76e606c05802009b9b14faf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612218"
---
# <span data-ttu-id="34055-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="34055-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="34055-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34055-102">SYNOPSIS</span></span>
<span data-ttu-id="34055-103">取得 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="34055-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="34055-104">句法</span><span class="sxs-lookup"><span data-stu-id="34055-104">SYNTAX</span></span>

### <span data-ttu-id="34055-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="34055-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34055-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="34055-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34055-107">說明</span><span class="sxs-lookup"><span data-stu-id="34055-107">DESCRIPTION</span></span>
<span data-ttu-id="34055-108">取得 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="34055-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="34055-109">您可以列出所有按鍵，或依據特定的索引鍵名稱來篩選清單。</span><span class="sxs-lookup"><span data-stu-id="34055-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="34055-110">示例</span><span class="sxs-lookup"><span data-stu-id="34055-110">EXAMPLES</span></span>

### <span data-ttu-id="34055-111">範例1取得所有按鍵</span><span class="sxs-lookup"><span data-stu-id="34055-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="34055-112">取得名為 "myiothub" 的 IotHub 的所有鍵</span><span class="sxs-lookup"><span data-stu-id="34055-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="34055-113">範例2取得特定金鑰的資訊</span><span class="sxs-lookup"><span data-stu-id="34055-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="34055-114">取得名為「iothubowner」的名為「myiothub」之 IotHub 的索引鍵資訊</span><span class="sxs-lookup"><span data-stu-id="34055-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="34055-115">參數</span><span class="sxs-lookup"><span data-stu-id="34055-115">PARAMETERS</span></span>

### <span data-ttu-id="34055-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34055-116">-DefaultProfile</span></span>
<span data-ttu-id="34055-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="34055-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34055-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="34055-118">-HubId</span></span>
<span data-ttu-id="34055-119">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="34055-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="34055-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="34055-120">-KeyName</span></span>
<span data-ttu-id="34055-121">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="34055-121">Name of the Key</span></span>

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

### <span data-ttu-id="34055-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="34055-122">-Name</span></span>
<span data-ttu-id="34055-123">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="34055-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="34055-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34055-124">-ResourceGroupName</span></span>
<span data-ttu-id="34055-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="34055-125">Resource Group Name</span></span>

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

### <span data-ttu-id="34055-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34055-126">CommonParameters</span></span>
<span data-ttu-id="34055-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34055-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34055-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="34055-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34055-129">輸入</span><span class="sxs-lookup"><span data-stu-id="34055-129">INPUTS</span></span>

### <span data-ttu-id="34055-130">System.object</span><span class="sxs-lookup"><span data-stu-id="34055-130">System.String</span></span>

## <span data-ttu-id="34055-131">輸出</span><span class="sxs-lookup"><span data-stu-id="34055-131">OUTPUTS</span></span>

### <span data-ttu-id="34055-132">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="34055-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="34055-133">筆記</span><span class="sxs-lookup"><span data-stu-id="34055-133">NOTES</span></span>

## <span data-ttu-id="34055-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="34055-134">RELATED LINKS</span></span>
