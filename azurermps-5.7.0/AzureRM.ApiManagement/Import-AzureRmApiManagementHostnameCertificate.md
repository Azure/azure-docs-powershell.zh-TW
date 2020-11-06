---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 98367100-4FFD-46F6-8974-603B32533626
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementhostnamecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
ms.openlocfilehash: 9c5f819a34ea0e394888e8156dad7a897d18167f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455556"
---
# <span data-ttu-id="2b1dc-101">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="2b1dc-101">Import-AzureRmApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="2b1dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="2b1dc-103">匯入 API 管理服務的 PFX 格式的憑證。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-103">Imports a certificate in a PFX format for an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b1dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b1dc-104">SYNTAX</span></span>

```
Import-AzureRmApiManagementHostnameCertificate -ResourceGroupName <String> -Name <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> -PfxPassword <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b1dc-105">說明</span><span class="sxs-lookup"><span data-stu-id="2b1dc-105">DESCRIPTION</span></span>
<span data-ttu-id="2b1dc-106">匯 **入-AzureRmApiManagementHostnameCertificate** Cmdlet 會以適用于 API 管理服務的 PFX 格式匯入憑證。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-106">The **Import-AzureRmApiManagementHostnameCertificate** cmdlet imports a certificate in a PFX format for an API Management Service.</span></span>
<span data-ttu-id="2b1dc-107">證書將用於自訂主機名稱設定。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-107">The certificate is to be used for custom hostnames configuration.</span></span>

## <span data-ttu-id="2b1dc-108">示例</span><span class="sxs-lookup"><span data-stu-id="2b1dc-108">EXAMPLES</span></span>

### <span data-ttu-id="2b1dc-109">範例1：匯入 API 管理主機名稱憑證</span><span class="sxs-lookup"><span data-stu-id="2b1dc-109">Example 1: Import a API Management hostname certificate</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName Contoso -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
```

<span data-ttu-id="2b1dc-110">這個命令會匯入 proxy 自訂主機名稱的憑證。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-110">This command imports a certificate for a proxy custom hostname.</span></span>

## <span data-ttu-id="2b1dc-111">參數</span><span class="sxs-lookup"><span data-stu-id="2b1dc-111">PARAMETERS</span></span>

### <span data-ttu-id="2b1dc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b1dc-112">-DefaultProfile</span></span>
<span data-ttu-id="2b1dc-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="2b1dc-114">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="2b1dc-114">-HostnameType</span></span>
<span data-ttu-id="2b1dc-115">指定此 Cmdlet 載入憑證的主機名稱類型。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-115">Specifies the host name type that this cmdlet loads the certificate for.</span></span>

<span data-ttu-id="2b1dc-116">有效值為：</span><span class="sxs-lookup"><span data-stu-id="2b1dc-116">Valid values are:</span></span> 

- <span data-ttu-id="2b1dc-117">Proxy</span><span class="sxs-lookup"><span data-stu-id="2b1dc-117">Proxy</span></span>
- <span data-ttu-id="2b1dc-118">門戶</span><span class="sxs-lookup"><span data-stu-id="2b1dc-118">Portal</span></span>

```yaml
Type: PsApiManagementHostnameType
Parameter Sets: (All)
Aliases: 
Accepted values: Proxy, Portal

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1dc-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b1dc-119">-Name</span></span>
<span data-ttu-id="2b1dc-120">指定此 Cmdlet 所匯入的 API 管理部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-120">Specifies the name of the API Management deployment that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1dc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b1dc-121">-PassThru</span></span>
<span data-ttu-id="2b1dc-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2b1dc-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1dc-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="2b1dc-124">-PfxPassword</span></span>
<span data-ttu-id="2b1dc-125">指定 .pfx 憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-125">Specifies the password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="2b1dc-126">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="2b1dc-126">-PfxPath</span></span>
<span data-ttu-id="2b1dc-127">指定 .pfx 憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-127">Specifies the path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="2b1dc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b1dc-128">-ResourceGroupName</span></span>
<span data-ttu-id="2b1dc-129">指定 API 管理部署所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-129">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1dc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b1dc-130">CommonParameters</span></span>
<span data-ttu-id="2b1dc-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b1dc-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b1dc-133">輸入</span><span class="sxs-lookup"><span data-stu-id="2b1dc-133">INPUTS</span></span>

### <span data-ttu-id="2b1dc-134">所有</span><span class="sxs-lookup"><span data-stu-id="2b1dc-134">None</span></span>
<span data-ttu-id="2b1dc-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b1dc-136">輸出</span><span class="sxs-lookup"><span data-stu-id="2b1dc-136">OUTPUTS</span></span>

### <span data-ttu-id="2b1dc-137">PsApiManagementHostnameCertificate 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="2b1dc-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="2b1dc-138">筆記</span><span class="sxs-lookup"><span data-stu-id="2b1dc-138">NOTES</span></span>

## <span data-ttu-id="2b1dc-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b1dc-139">RELATED LINKS</span></span>

[<span data-ttu-id="2b1dc-140">新-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b1dc-140">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)

[<span data-ttu-id="2b1dc-141">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="2b1dc-141">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


