---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: ECF85C07-2C9E-487D-A2ED-77875C380244
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/save-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 8dd9aeaaf987fba155ca80b0c8739d44c80945e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447650"
---
# <span data-ttu-id="e4f07-101">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="e4f07-101">Save-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="e4f07-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4f07-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f07-103">下載伺服器管理閘道的設定檔，並將它儲存到本機檔案。</span><span class="sxs-lookup"><span data-stu-id="e4f07-103">Downloads the profile for a Server Management gateway and saves it to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4f07-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4f07-104">SYNTAX</span></span>

### <span data-ttu-id="e4f07-105">ByName</span><span class="sxs-lookup"><span data-stu-id="e4f07-105">ByName</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-ResourceGroupName] <String>
 [-GatewayName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4f07-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="e4f07-106">ByObject</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-Gateway] <Gateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4f07-107">說明</span><span class="sxs-lookup"><span data-stu-id="e4f07-107">DESCRIPTION</span></span>
<span data-ttu-id="e4f07-108">**AzureRmServerManagementGatewayProfile** Cmdlet 會下載 Azure Server 管理閘道的設定檔，並將它儲存到本機檔案。</span><span class="sxs-lookup"><span data-stu-id="e4f07-108">The **Save-AzureRmServerManagementGatewayProfile** cmdlet downloads the profile for an Azure Server Management gateway and stores it to a local file.</span></span>

## <span data-ttu-id="e4f07-109">示例</span><span class="sxs-lookup"><span data-stu-id="e4f07-109">EXAMPLES</span></span>

## <span data-ttu-id="e4f07-110">參數</span><span class="sxs-lookup"><span data-stu-id="e4f07-110">PARAMETERS</span></span>

### <span data-ttu-id="e4f07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f07-111">-DefaultProfile</span></span>
<span data-ttu-id="e4f07-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4f07-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4f07-113">-閘道</span><span class="sxs-lookup"><span data-stu-id="e4f07-113">-Gateway</span></span>
<span data-ttu-id="e4f07-114">指定此 Cmdlet 取得其設定檔的閘道。</span><span class="sxs-lookup"><span data-stu-id="e4f07-114">Specifies the gateway that this cmdlet gets the profile for.</span></span>

<span data-ttu-id="e4f07-115">可以使用，而不是指定 ResourceGroupName 和 GatewayName</span><span class="sxs-lookup"><span data-stu-id="e4f07-115">May be used instead of specifying ResourceGroupName and GatewayName</span></span>

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

### <span data-ttu-id="e4f07-116">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="e4f07-116">-GatewayName</span></span>
<span data-ttu-id="e4f07-117">指定此 Cmdlet 取得其設定檔的閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="e4f07-117">Specifies the name of the gateway that this cmdlet gets the profile for.</span></span>

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

### <span data-ttu-id="e4f07-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="e4f07-118">-OutputFile</span></span>
<span data-ttu-id="e4f07-119">指定要儲存設定檔資料的本機檔案。</span><span class="sxs-lookup"><span data-stu-id="e4f07-119">Specifies the local file in which to save the profile data.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f07-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4f07-120">-ResourceGroupName</span></span>
<span data-ttu-id="e4f07-121">指定閘道所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4f07-121">Specifies the name of the resource group that the gateway belongs to.</span></span>

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

### <span data-ttu-id="e4f07-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f07-122">CommonParameters</span></span>
<span data-ttu-id="e4f07-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4f07-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f07-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4f07-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f07-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e4f07-125">INPUTS</span></span>

### <span data-ttu-id="e4f07-126">關</span><span class="sxs-lookup"><span data-stu-id="e4f07-126">Gateway</span></span>
<span data-ttu-id="e4f07-127">參數 "閘道" 接受管線中 "Gateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e4f07-127">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="e4f07-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e4f07-128">OUTPUTS</span></span>

### <span data-ttu-id="e4f07-129">FileInfo</span><span class="sxs-lookup"><span data-stu-id="e4f07-129">System.IO.FileInfo</span></span>

## <span data-ttu-id="e4f07-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e4f07-130">NOTES</span></span>

## <span data-ttu-id="e4f07-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4f07-131">RELATED LINKS</span></span>

[<span data-ttu-id="e4f07-132">安裝-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="e4f07-132">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="e4f07-133">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="e4f07-133">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)


