---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22B63259-799B-4F25-A06B-7A818D295870
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/reset-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 0833266bcd6e98a1d9744db2bc202bce5a01f3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447655"
---
# <span data-ttu-id="a98cc-101">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="a98cc-101">Reset-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="a98cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a98cc-102">SYNOPSIS</span></span>
<span data-ttu-id="a98cc-103">重設伺服器管理閘道的設定檔。</span><span class="sxs-lookup"><span data-stu-id="a98cc-103">Resets the profile of a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a98cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="a98cc-104">SYNTAX</span></span>

### <span data-ttu-id="a98cc-105">ByName</span><span class="sxs-lookup"><span data-stu-id="a98cc-105">ByName</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a98cc-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="a98cc-106">ByObject</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a98cc-107">說明</span><span class="sxs-lookup"><span data-stu-id="a98cc-107">DESCRIPTION</span></span>
<span data-ttu-id="a98cc-108">**Reset AzureRmServerManagementGatewayProfile** Cmdlet 會重設 Azure Server 管理閘道的設定檔。</span><span class="sxs-lookup"><span data-stu-id="a98cc-108">The **Reset-AzureRmServerManagementGatewayProfile** cmdlet resets the profile for an Azure Server Management Gateway.</span></span>

<span data-ttu-id="a98cc-109">您必須使用 Save-AzureRmServerManagementGatewayProfile Cmdlet 來下載設定檔，然後再使用 Install-AzureRmServerManagementGatewayProfile Cmdlet，在您重設設定檔之後進行儲存。</span><span class="sxs-lookup"><span data-stu-id="a98cc-109">You will need to use the Save-AzureRmServerManagementGatewayProfile cmdlet to download the profile and then the Install-AzureRmServerManagementGatewayProfile cmdlet to save it after you reset the profile.</span></span>

## <span data-ttu-id="a98cc-110">示例</span><span class="sxs-lookup"><span data-stu-id="a98cc-110">EXAMPLES</span></span>

## <span data-ttu-id="a98cc-111">參數</span><span class="sxs-lookup"><span data-stu-id="a98cc-111">PARAMETERS</span></span>

### <span data-ttu-id="a98cc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a98cc-112">-DefaultProfile</span></span>
<span data-ttu-id="a98cc-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a98cc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a98cc-114">-閘道</span><span class="sxs-lookup"><span data-stu-id="a98cc-114">-Gateway</span></span>
<span data-ttu-id="a98cc-115">指定 Cmdlet 針對其重設設定檔的閘道。</span><span class="sxs-lookup"><span data-stu-id="a98cc-115">Specifies the gateway for which the cmdlet resets the profile for.</span></span>

<span data-ttu-id="a98cc-116">可以指定，而不是 ResourceGoupName 和 GatewayName</span><span class="sxs-lookup"><span data-stu-id="a98cc-116">May be specified instead of ResourceGoupName and GatewayName</span></span>

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

### <span data-ttu-id="a98cc-117">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="a98cc-117">-GatewayName</span></span>
<span data-ttu-id="a98cc-118">指定 Cmdlet 重設設定檔的閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="a98cc-118">Specifies the name of the gateway for which the cmdlet resets the profile.</span></span>

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

### <span data-ttu-id="a98cc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a98cc-119">-ResourceGroupName</span></span>
<span data-ttu-id="a98cc-120">指定閘道所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a98cc-120">Specifies the name of the resource group that the gateway belongs to.</span></span>

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

### <span data-ttu-id="a98cc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a98cc-121">CommonParameters</span></span>
<span data-ttu-id="a98cc-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a98cc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a98cc-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a98cc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a98cc-124">輸入</span><span class="sxs-lookup"><span data-stu-id="a98cc-124">INPUTS</span></span>

### <span data-ttu-id="a98cc-125">關</span><span class="sxs-lookup"><span data-stu-id="a98cc-125">Gateway</span></span>
<span data-ttu-id="a98cc-126">參數 "閘道" 接受管線中 "Gateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a98cc-126">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="a98cc-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a98cc-127">OUTPUTS</span></span>

## <span data-ttu-id="a98cc-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a98cc-128">NOTES</span></span>

## <span data-ttu-id="a98cc-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a98cc-129">RELATED LINKS</span></span>

[<span data-ttu-id="a98cc-130">安裝-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="a98cc-130">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="a98cc-131">儲存-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="a98cc-131">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


