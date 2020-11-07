---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: f73d53fc3031fc72be950547e5b9c2b93a9a0079
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623804"
---
# <span data-ttu-id="cf4d5-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="cf4d5-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="cf4d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf4d5-102">SYNOPSIS</span></span>
<span data-ttu-id="cf4d5-103">建立伺服器管理閘道。</span><span class="sxs-lookup"><span data-stu-id="cf4d5-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf4d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf4d5-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf4d5-105">說明</span><span class="sxs-lookup"><span data-stu-id="cf4d5-105">DESCRIPTION</span></span>
<span data-ttu-id="cf4d5-106">**新的-AzureRmServerManagementGateway** Cmdlet 會建立 Azure Server 管理閘道。</span><span class="sxs-lookup"><span data-stu-id="cf4d5-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="cf4d5-107">示例</span><span class="sxs-lookup"><span data-stu-id="cf4d5-107">EXAMPLES</span></span>

## <span data-ttu-id="cf4d5-108">參數</span><span class="sxs-lookup"><span data-stu-id="cf4d5-108">PARAMETERS</span></span>

### <span data-ttu-id="cf4d5-109">-AutoUpgrade</span><span class="sxs-lookup"><span data-stu-id="cf4d5-109">-AutoUpgrade</span></span>
<span data-ttu-id="cf4d5-110">表示新版本發行時，閘道會自動升級本身。</span><span class="sxs-lookup"><span data-stu-id="cf4d5-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf4d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf4d5-111">-DefaultProfile</span></span>
<span data-ttu-id="cf4d5-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf4d5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf4d5-113">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="cf4d5-113">-GatewayName</span></span>
<span data-ttu-id="cf4d5-114">指定此 Cmdlet 所建立之閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf4d5-114">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf4d5-115">-位置</span><span class="sxs-lookup"><span data-stu-id="cf4d5-115">-Location</span></span>
<span data-ttu-id="cf4d5-116">指定要建立閘道的位置。</span><span class="sxs-lookup"><span data-stu-id="cf4d5-116">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf4d5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf4d5-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf4d5-118">指定此 Cmdlet 建立閘道所用之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf4d5-118">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf4d5-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="cf4d5-119">-Tag</span></span>
<span data-ttu-id="cf4d5-120">與閘道相關聯的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="cf4d5-120">Key/value pairs associated with the gateway.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf4d5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf4d5-121">CommonParameters</span></span>
<span data-ttu-id="cf4d5-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf4d5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf4d5-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf4d5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf4d5-124">輸入</span><span class="sxs-lookup"><span data-stu-id="cf4d5-124">INPUTS</span></span>

### <span data-ttu-id="cf4d5-125">所有</span><span class="sxs-lookup"><span data-stu-id="cf4d5-125">None</span></span>
<span data-ttu-id="cf4d5-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="cf4d5-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cf4d5-127">輸出</span><span class="sxs-lookup"><span data-stu-id="cf4d5-127">OUTPUTS</span></span>

### <span data-ttu-id="cf4d5-128">[ServerManagement] 閘道</span><span class="sxs-lookup"><span data-stu-id="cf4d5-128">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="cf4d5-129">筆記</span><span class="sxs-lookup"><span data-stu-id="cf4d5-129">NOTES</span></span>

## <span data-ttu-id="cf4d5-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf4d5-130">RELATED LINKS</span></span>

[<span data-ttu-id="cf4d5-131">AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="cf4d5-131">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="cf4d5-132">移除-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="cf4d5-132">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


