---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: ac56d5392025a85d0310862a1786dde3d0f8ca2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787542"
---
# <span data-ttu-id="28323-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="28323-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="28323-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28323-102">SYNOPSIS</span></span>
<span data-ttu-id="28323-103">取得 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="28323-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="28323-104">句法</span><span class="sxs-lookup"><span data-stu-id="28323-104">SYNTAX</span></span>

```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28323-105">說明</span><span class="sxs-lookup"><span data-stu-id="28323-105">DESCRIPTION</span></span>
<span data-ttu-id="28323-106">取得 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="28323-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="28323-107">您可以列出所有按鍵，或依據特定的索引鍵名稱來篩選清單。</span><span class="sxs-lookup"><span data-stu-id="28323-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="28323-108">示例</span><span class="sxs-lookup"><span data-stu-id="28323-108">EXAMPLES</span></span>

### <span data-ttu-id="28323-109">範例1取得所有按鍵</span><span class="sxs-lookup"><span data-stu-id="28323-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="28323-110">取得名為 "myiothub" 的 IotHub 的所有鍵</span><span class="sxs-lookup"><span data-stu-id="28323-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="28323-111">範例2取得特定金鑰的資訊</span><span class="sxs-lookup"><span data-stu-id="28323-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="28323-112">取得名為「iothubowner」的名為「myiothub」之 IotHub 的索引鍵資訊</span><span class="sxs-lookup"><span data-stu-id="28323-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="28323-113">參數</span><span class="sxs-lookup"><span data-stu-id="28323-113">PARAMETERS</span></span>

### <span data-ttu-id="28323-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28323-114">-DefaultProfile</span></span>
<span data-ttu-id="28323-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="28323-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28323-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="28323-116">-KeyName</span></span>
<span data-ttu-id="28323-117">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="28323-117">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28323-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="28323-118">-Name</span></span>
<span data-ttu-id="28323-119">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="28323-119">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28323-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28323-120">-ResourceGroupName</span></span>
<span data-ttu-id="28323-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="28323-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28323-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28323-122">CommonParameters</span></span>
<span data-ttu-id="28323-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28323-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28323-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="28323-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28323-125">輸入</span><span class="sxs-lookup"><span data-stu-id="28323-125">INPUTS</span></span>

### <span data-ttu-id="28323-126">System.object</span><span class="sxs-lookup"><span data-stu-id="28323-126">System.String</span></span>

## <span data-ttu-id="28323-127">輸出</span><span class="sxs-lookup"><span data-stu-id="28323-127">OUTPUTS</span></span>

### <span data-ttu-id="28323-128">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="28323-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="28323-129">筆記</span><span class="sxs-lookup"><span data-stu-id="28323-129">NOTES</span></span>

## <span data-ttu-id="28323-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="28323-130">RELATED LINKS</span></span>
