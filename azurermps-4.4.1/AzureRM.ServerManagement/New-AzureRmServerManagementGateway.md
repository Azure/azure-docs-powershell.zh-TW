---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9cb98b9671f43ddd7acbcc84e8473a12da00f405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449516"
---
# <span data-ttu-id="ad414-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="ad414-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="ad414-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad414-102">SYNOPSIS</span></span>
<span data-ttu-id="ad414-103">建立伺服器管理閘道。</span><span class="sxs-lookup"><span data-stu-id="ad414-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad414-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad414-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad414-105">說明</span><span class="sxs-lookup"><span data-stu-id="ad414-105">DESCRIPTION</span></span>
<span data-ttu-id="ad414-106">**新的-AzureRmServerManagementGateway** Cmdlet 會建立 Azure Server 管理閘道。</span><span class="sxs-lookup"><span data-stu-id="ad414-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="ad414-107">示例</span><span class="sxs-lookup"><span data-stu-id="ad414-107">EXAMPLES</span></span>

## <span data-ttu-id="ad414-108">參數</span><span class="sxs-lookup"><span data-stu-id="ad414-108">PARAMETERS</span></span>

### <span data-ttu-id="ad414-109">-AutoUpgrade</span><span class="sxs-lookup"><span data-stu-id="ad414-109">-AutoUpgrade</span></span>
<span data-ttu-id="ad414-110">表示新版本發行時，閘道會自動升級本身。</span><span class="sxs-lookup"><span data-stu-id="ad414-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad414-111">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="ad414-111">-GatewayName</span></span>
<span data-ttu-id="ad414-112">指定此 Cmdlet 所建立之閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad414-112">Specifies the name of the gateway that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ad414-113">-位置</span><span class="sxs-lookup"><span data-stu-id="ad414-113">-Location</span></span>
<span data-ttu-id="ad414-114">指定要建立閘道的位置。</span><span class="sxs-lookup"><span data-stu-id="ad414-114">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad414-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad414-115">-ResourceGroupName</span></span>
<span data-ttu-id="ad414-116">指定此 Cmdlet 建立閘道所用之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad414-116">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

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

### <span data-ttu-id="ad414-117">-標記</span><span class="sxs-lookup"><span data-stu-id="ad414-117">-Tags</span></span>
<span data-ttu-id="ad414-118">將標記指定為鍵值對。</span><span class="sxs-lookup"><span data-stu-id="ad414-118">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="ad414-119">您可以使用標籤來找出來自其他 Azure 資源的閘道。</span><span class="sxs-lookup"><span data-stu-id="ad414-119">You can use tags to identify a Gateway from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad414-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad414-120">-DefaultProfile</span></span>
<span data-ttu-id="ad414-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad414-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad414-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad414-122">CommonParameters</span></span>
<span data-ttu-id="ad414-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad414-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad414-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad414-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad414-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ad414-125">INPUTS</span></span>

## <span data-ttu-id="ad414-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ad414-126">OUTPUTS</span></span>

### <span data-ttu-id="ad414-127">[ServerManagement] 閘道</span><span class="sxs-lookup"><span data-stu-id="ad414-127">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="ad414-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ad414-128">NOTES</span></span>

## <span data-ttu-id="ad414-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad414-129">RELATED LINKS</span></span>

[<span data-ttu-id="ad414-130">AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="ad414-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="ad414-131">移除-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="ad414-131">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


