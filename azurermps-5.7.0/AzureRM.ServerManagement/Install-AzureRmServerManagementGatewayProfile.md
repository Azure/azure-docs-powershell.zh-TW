---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/install-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b9563e9b8b7afb7b980f0b3cd307c76fb9c6e8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447660"
---
# <span data-ttu-id="7c5a1-101">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="7c5a1-101">Install-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="7c5a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c5a1-102">SYNOPSIS</span></span>
<span data-ttu-id="7c5a1-103">安裝伺服器管理閘道設定檔。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-103">Installs a Server Management Gateway profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c5a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c5a1-104">SYNTAX</span></span>

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c5a1-105">說明</span><span class="sxs-lookup"><span data-stu-id="7c5a1-105">DESCRIPTION</span></span>
<span data-ttu-id="7c5a1-106">**AzureRmServerManagementGatewayProfile** Cmdlet 會將 Azure Server 管理閘道設定檔安裝至正確的位置。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-106">The **Install-AzureRmServerManagementGatewayProfile** cmdlet installs an Azure Server Management Gateway profile into the correct location.</span></span>
<span data-ttu-id="7c5a1-107">此 Cmdlet 安裝的檔案會命名為 [profile.js]。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-107">The file that this cmdlet installs is named profile.json.</span></span>

## <span data-ttu-id="7c5a1-108">示例</span><span class="sxs-lookup"><span data-stu-id="7c5a1-108">EXAMPLES</span></span>

## <span data-ttu-id="7c5a1-109">參數</span><span class="sxs-lookup"><span data-stu-id="7c5a1-109">PARAMETERS</span></span>

### <span data-ttu-id="7c5a1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c5a1-110">-DefaultProfile</span></span>
<span data-ttu-id="7c5a1-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c5a1-112">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7c5a1-112">-InputFile</span></span>
<span data-ttu-id="7c5a1-113">指定內含要安裝之閘道設定檔的本機檔案名。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-113">Specifies the name of the local file that contains the gateway profile to install.</span></span>

<span data-ttu-id="7c5a1-114">此 Cmdlet 安裝的檔案先前應該已使用 Save-AzureRmServerManagementGatewayProfile Cmdlet 進行儲存。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-114">The file that this cmdlet installs should have been previously saved with the Save-AzureRmServerManagementGatewayProfile cmdlet.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c5a1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c5a1-115">CommonParameters</span></span>
<span data-ttu-id="7c5a1-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c5a1-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c5a1-118">輸入</span><span class="sxs-lookup"><span data-stu-id="7c5a1-118">INPUTS</span></span>

### <span data-ttu-id="7c5a1-119">FileInfo</span><span class="sxs-lookup"><span data-stu-id="7c5a1-119">FileInfo</span></span>
<span data-ttu-id="7c5a1-120">形參 "InputFile" 接受管線中 "FileInfo" 類型的值</span><span class="sxs-lookup"><span data-stu-id="7c5a1-120">Parameter 'InputFile' accepts value of type 'FileInfo' from the pipeline</span></span>

## <span data-ttu-id="7c5a1-121">輸出</span><span class="sxs-lookup"><span data-stu-id="7c5a1-121">OUTPUTS</span></span>

## <span data-ttu-id="7c5a1-122">筆記</span><span class="sxs-lookup"><span data-stu-id="7c5a1-122">NOTES</span></span>

## <span data-ttu-id="7c5a1-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c5a1-123">RELATED LINKS</span></span>

[<span data-ttu-id="7c5a1-124">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="7c5a1-124">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="7c5a1-125">儲存-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="7c5a1-125">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


