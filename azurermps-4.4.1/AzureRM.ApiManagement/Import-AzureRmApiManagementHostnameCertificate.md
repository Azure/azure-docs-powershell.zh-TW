---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98367100-4FFD-46F6-8974-603B32533626
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
ms.openlocfilehash: 5d931551491a0df67252f90f6052fdebde15492b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624224"
---
# <span data-ttu-id="c9e63-101">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="c9e63-101">Import-AzureRmApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="c9e63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9e63-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e63-103">匯入 API 管理服務的 PFX 格式的憑證。</span><span class="sxs-lookup"><span data-stu-id="c9e63-103">Imports a certificate in a PFX format for an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9e63-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9e63-104">SYNTAX</span></span>

```
Import-AzureRmApiManagementHostnameCertificate -ResourceGroupName <String> -Name <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> -PfxPassword <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9e63-105">說明</span><span class="sxs-lookup"><span data-stu-id="c9e63-105">DESCRIPTION</span></span>
<span data-ttu-id="c9e63-106">匯 **入-AzureRmApiManagementHostnameCertificate** Cmdlet 會以適用于 API 管理服務的 PFX 格式匯入憑證。</span><span class="sxs-lookup"><span data-stu-id="c9e63-106">The **Import-AzureRmApiManagementHostnameCertificate** cmdlet imports a certificate in a PFX format for an API Management Service.</span></span>
<span data-ttu-id="c9e63-107">證書將用於自訂主機名稱設定。</span><span class="sxs-lookup"><span data-stu-id="c9e63-107">The certificate is to be used for custom hostnames configuration.</span></span>

## <span data-ttu-id="c9e63-108">示例</span><span class="sxs-lookup"><span data-stu-id="c9e63-108">EXAMPLES</span></span>

### <span data-ttu-id="c9e63-109">範例1：匯入 API 管理主機名稱憑證</span><span class="sxs-lookup"><span data-stu-id="c9e63-109">Example 1: Import a API Management hostname certificate</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName Contoso -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
```

<span data-ttu-id="c9e63-110">這個命令會匯入 proxy 自訂主機名稱的憑證。</span><span class="sxs-lookup"><span data-stu-id="c9e63-110">This command imports a certificate for a proxy custom hostname.</span></span>

## <span data-ttu-id="c9e63-111">參數</span><span class="sxs-lookup"><span data-stu-id="c9e63-111">PARAMETERS</span></span>

### <span data-ttu-id="c9e63-112">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="c9e63-112">-HostnameType</span></span>
<span data-ttu-id="c9e63-113">指定此 Cmdlet 載入憑證的主機名稱類型。</span><span class="sxs-lookup"><span data-stu-id="c9e63-113">Specifies the host name type that this cmdlet loads the certificate for.</span></span>

<span data-ttu-id="c9e63-114">有效值為：</span><span class="sxs-lookup"><span data-stu-id="c9e63-114">Valid values are:</span></span> 

- <span data-ttu-id="c9e63-115">Proxy</span><span class="sxs-lookup"><span data-stu-id="c9e63-115">Proxy</span></span>
- <span data-ttu-id="c9e63-116">門戶</span><span class="sxs-lookup"><span data-stu-id="c9e63-116">Portal</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases: 
Accepted values: Proxy, Portal

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e63-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9e63-117">-Name</span></span>
<span data-ttu-id="c9e63-118">指定此 Cmdlet 所匯入的 API 管理部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9e63-118">Specifies the name of the API Management deployment that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e63-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9e63-119">-PassThru</span></span>
<span data-ttu-id="c9e63-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="c9e63-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c9e63-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c9e63-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e63-122">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="c9e63-122">-PfxPassword</span></span>
<span data-ttu-id="c9e63-123">指定 .pfx 憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="c9e63-123">Specifies the password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="c9e63-124">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="c9e63-124">-PfxPath</span></span>
<span data-ttu-id="c9e63-125">指定 .pfx 憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c9e63-125">Specifies the path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="c9e63-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9e63-126">-ResourceGroupName</span></span>
<span data-ttu-id="c9e63-127">指定 API 管理部署所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9e63-127">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e63-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9e63-128">-DefaultProfile</span></span>
<span data-ttu-id="c9e63-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9e63-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9e63-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e63-130">CommonParameters</span></span>
<span data-ttu-id="c9e63-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9e63-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e63-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c9e63-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e63-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c9e63-133">INPUTS</span></span>

## <span data-ttu-id="c9e63-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c9e63-134">OUTPUTS</span></span>

### <span data-ttu-id="c9e63-135">PsApiManagementHostnameCertificate 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="c9e63-135">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="c9e63-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c9e63-136">NOTES</span></span>

## <span data-ttu-id="c9e63-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9e63-137">RELATED LINKS</span></span>

[<span data-ttu-id="c9e63-138">新-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9e63-138">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)

[<span data-ttu-id="c9e63-139">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="c9e63-139">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)

