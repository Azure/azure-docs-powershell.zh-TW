---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 41F8F851-6F9F-4DA4-8CE6-D8C9B7CF68D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
ms.openlocfilehash: 53bf195bf801b4746f0ea958949f1683c8ca3d0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624990"
---
# <span data-ttu-id="315f9-101">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="315f9-101">Remove-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="315f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="315f9-102">SYNOPSIS</span></span>
<span data-ttu-id="315f9-103">移除伺服器管理閘道。</span><span class="sxs-lookup"><span data-stu-id="315f9-103">Removes a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="315f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="315f9-104">SYNTAX</span></span>

### <span data-ttu-id="315f9-105">ByName</span><span class="sxs-lookup"><span data-stu-id="315f9-105">ByName</span></span>
```
Remove-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="315f9-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="315f9-106">ByObject</span></span>
```
Remove-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="315f9-107">說明</span><span class="sxs-lookup"><span data-stu-id="315f9-107">DESCRIPTION</span></span>
<span data-ttu-id="315f9-108">**AzureRmServerManagementGateway** Cmdlet 會移除 Azure 伺服器管理閘道。</span><span class="sxs-lookup"><span data-stu-id="315f9-108">The **Remove-AzureRmServerManagementGateway** cmdlet removes an Azure Server Management gateway.</span></span>

## <span data-ttu-id="315f9-109">示例</span><span class="sxs-lookup"><span data-stu-id="315f9-109">EXAMPLES</span></span>

## <span data-ttu-id="315f9-110">參數</span><span class="sxs-lookup"><span data-stu-id="315f9-110">PARAMETERS</span></span>

### <span data-ttu-id="315f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="315f9-111">-DefaultProfile</span></span>
<span data-ttu-id="315f9-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="315f9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="315f9-113">-閘道</span><span class="sxs-lookup"><span data-stu-id="315f9-113">-Gateway</span></span>
<span data-ttu-id="315f9-114">指定此 Cmdlet 移除的閘道。</span><span class="sxs-lookup"><span data-stu-id="315f9-114">Specifies the gateway that this cmdlet removes.</span></span>

<span data-ttu-id="315f9-115">您可以使用這個參數，而不是 *ResourceGroupName* 和 *GatewayName* 參數。</span><span class="sxs-lookup"><span data-stu-id="315f9-115">This parameter may be used instead of the *ResourceGroupName* and the *GatewayName* parameters.</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="315f9-116">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="315f9-116">-GatewayName</span></span>
<span data-ttu-id="315f9-117">指定此 Cmdlet 移除的閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="315f9-117">Specifies the name of the gateway that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="315f9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="315f9-118">-ResourceGroupName</span></span>
<span data-ttu-id="315f9-119">指定閘道所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="315f9-119">Specifies the name of the resource group in that the gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="315f9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="315f9-120">CommonParameters</span></span>
<span data-ttu-id="315f9-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="315f9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="315f9-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="315f9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="315f9-123">輸入</span><span class="sxs-lookup"><span data-stu-id="315f9-123">INPUTS</span></span>

### <span data-ttu-id="315f9-124">關</span><span class="sxs-lookup"><span data-stu-id="315f9-124">Gateway</span></span>
<span data-ttu-id="315f9-125">參數 "閘道" 接受管線中 "Gateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="315f9-125">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="315f9-126">輸出</span><span class="sxs-lookup"><span data-stu-id="315f9-126">OUTPUTS</span></span>

## <span data-ttu-id="315f9-127">筆記</span><span class="sxs-lookup"><span data-stu-id="315f9-127">NOTES</span></span>
* <span data-ttu-id="315f9-128">您必須先移除閘道中的所有節點，才能使用這個 Cmdlet;否則這個 Cmdlet 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="315f9-128">All the nodes in the Gateway must be removed before using this cmdlet; otherwise this cmdlet will fail.</span></span>

## <span data-ttu-id="315f9-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="315f9-129">RELATED LINKS</span></span>

[<span data-ttu-id="315f9-130">AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="315f9-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="315f9-131">新-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="315f9-131">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)


