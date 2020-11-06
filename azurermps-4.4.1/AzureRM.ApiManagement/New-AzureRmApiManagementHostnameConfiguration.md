---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: 1b34903f402f7e8d432d16087f1e32fc7b7da3e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450105"
---
# <span data-ttu-id="982d0-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="982d0-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="982d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="982d0-102">SYNOPSIS</span></span>
<span data-ttu-id="982d0-103">建立 PsApiManagementHostnameConfiguration 的實例。</span><span class="sxs-lookup"><span data-stu-id="982d0-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="982d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="982d0-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="982d0-105">說明</span><span class="sxs-lookup"><span data-stu-id="982d0-105">DESCRIPTION</span></span>
<span data-ttu-id="982d0-106">**新的 AzureRmApiManagementHostnameConfiguration** Cmdlet 是一個協助程式命令，可建立 **PsApiManagementHostnameConfiguration** 的實例。</span><span class="sxs-lookup"><span data-stu-id="982d0-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="982d0-107">此命令與 Set-AzureRmApiManagementHostnames Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="982d0-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="982d0-108">示例</span><span class="sxs-lookup"><span data-stu-id="982d0-108">EXAMPLES</span></span>

### <span data-ttu-id="982d0-109">範例1：建立和初始化 PsApiManagementHostnameConfiguration 的實例</span><span class="sxs-lookup"><span data-stu-id="982d0-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="982d0-110">這個命令會建立並初始化 **PsApiManagementHostnameConfiguration** 的實例。</span><span class="sxs-lookup"><span data-stu-id="982d0-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="982d0-111">參數</span><span class="sxs-lookup"><span data-stu-id="982d0-111">PARAMETERS</span></span>

### <span data-ttu-id="982d0-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="982d0-112">-CertificateThumbprint</span></span>
<span data-ttu-id="982d0-113">指定憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="982d0-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="982d0-114">您必須先使用 Import-AzureRmApiManagementHostnameCertificate Cmdlet 匯入憑證。</span><span class="sxs-lookup"><span data-stu-id="982d0-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="982d0-115">-Hostname</span><span class="sxs-lookup"><span data-stu-id="982d0-115">-Hostname</span></span>
<span data-ttu-id="982d0-116">指定此 Cmdlet 為其建立 **PsApiManagementHostnameConfiguration** 實例的自訂主機名稱。</span><span class="sxs-lookup"><span data-stu-id="982d0-116">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="982d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="982d0-117">-DefaultProfile</span></span>
<span data-ttu-id="982d0-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="982d0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="982d0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="982d0-119">CommonParameters</span></span>
<span data-ttu-id="982d0-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="982d0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="982d0-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="982d0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="982d0-122">輸入</span><span class="sxs-lookup"><span data-stu-id="982d0-122">INPUTS</span></span>

## <span data-ttu-id="982d0-123">輸出</span><span class="sxs-lookup"><span data-stu-id="982d0-123">OUTPUTS</span></span>

### <span data-ttu-id="982d0-124">PsApiManagementHostnameConfiguration 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="982d0-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="982d0-125">筆記</span><span class="sxs-lookup"><span data-stu-id="982d0-125">NOTES</span></span>

## <span data-ttu-id="982d0-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="982d0-126">RELATED LINKS</span></span>

[<span data-ttu-id="982d0-127">匯入-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="982d0-127">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="982d0-128">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="982d0-128">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


