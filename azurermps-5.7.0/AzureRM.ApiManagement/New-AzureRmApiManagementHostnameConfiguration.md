---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: 066538db3a763c5a3c6d9de9f621ca2b81552983
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444831"
---
# <span data-ttu-id="e8f1c-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8f1c-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="e8f1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f1c-103">建立 PsApiManagementHostnameConfiguration 的實例。</span><span class="sxs-lookup"><span data-stu-id="e8f1c-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8f1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8f1c-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8f1c-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8f1c-105">DESCRIPTION</span></span>
<span data-ttu-id="e8f1c-106">**新的 AzureRmApiManagementHostnameConfiguration** Cmdlet 是一個協助程式命令，可建立 **PsApiManagementHostnameConfiguration** 的實例。</span><span class="sxs-lookup"><span data-stu-id="e8f1c-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="e8f1c-107">此命令與 Set-AzureRmApiManagementHostnames Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="e8f1c-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="e8f1c-108">示例</span><span class="sxs-lookup"><span data-stu-id="e8f1c-108">EXAMPLES</span></span>

### <span data-ttu-id="e8f1c-109">範例1：建立和初始化 PsApiManagementHostnameConfiguration 的實例</span><span class="sxs-lookup"><span data-stu-id="e8f1c-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="e8f1c-110">這個命令會建立並初始化 **PsApiManagementHostnameConfiguration** 的實例。</span><span class="sxs-lookup"><span data-stu-id="e8f1c-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="e8f1c-111">參數</span><span class="sxs-lookup"><span data-stu-id="e8f1c-111">PARAMETERS</span></span>

### <span data-ttu-id="e8f1c-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e8f1c-112">-CertificateThumbprint</span></span>
<span data-ttu-id="e8f1c-113">指定憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="e8f1c-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="e8f1c-114">您必須先使用 Import-AzureRmApiManagementHostnameCertificate Cmdlet 匯入憑證。</span><span class="sxs-lookup"><span data-stu-id="e8f1c-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f1c-115">-DefaultProfile</span></span>
<span data-ttu-id="e8f1c-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8f1c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e8f1c-117">-Hostname</span><span class="sxs-lookup"><span data-stu-id="e8f1c-117">-Hostname</span></span>
<span data-ttu-id="e8f1c-118">指定此 Cmdlet 為其建立 **PsApiManagementHostnameConfiguration** 實例的自訂主機名稱。</span><span class="sxs-lookup"><span data-stu-id="e8f1c-118">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f1c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f1c-119">CommonParameters</span></span>
<span data-ttu-id="e8f1c-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8f1c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f1c-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8f1c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f1c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e8f1c-122">INPUTS</span></span>

### <span data-ttu-id="e8f1c-123">所有</span><span class="sxs-lookup"><span data-stu-id="e8f1c-123">None</span></span>
<span data-ttu-id="e8f1c-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e8f1c-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8f1c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e8f1c-125">OUTPUTS</span></span>

### <span data-ttu-id="e8f1c-126">PsApiManagementHostnameConfiguration 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="e8f1c-126">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="e8f1c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e8f1c-127">NOTES</span></span>

## <span data-ttu-id="e8f1c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8f1c-128">RELATED LINKS</span></span>

[<span data-ttu-id="e8f1c-129">匯入-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="e8f1c-129">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="e8f1c-130">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="e8f1c-130">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


