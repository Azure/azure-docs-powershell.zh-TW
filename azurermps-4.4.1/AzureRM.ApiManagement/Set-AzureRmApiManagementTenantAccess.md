---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: c75aceee59e5696d928f19fa6d5ae317828fa82f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445167"
---
# <span data-ttu-id="19642-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="19642-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="19642-102">摘要</span><span class="sxs-lookup"><span data-stu-id="19642-102">SYNOPSIS</span></span>
<span data-ttu-id="19642-103">啟用或停用租使用者存取。</span><span class="sxs-lookup"><span data-stu-id="19642-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19642-104">句法</span><span class="sxs-lookup"><span data-stu-id="19642-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19642-105">說明</span><span class="sxs-lookup"><span data-stu-id="19642-105">DESCRIPTION</span></span>
<span data-ttu-id="19642-106">**AzureRmApiManagementTenantAccess** Cmdlet 可啟用或停用租使用者存取。</span><span class="sxs-lookup"><span data-stu-id="19642-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="19642-107">示例</span><span class="sxs-lookup"><span data-stu-id="19642-107">EXAMPLES</span></span>

### <span data-ttu-id="19642-108">範例1：啟用租使用者存取</span><span class="sxs-lookup"><span data-stu-id="19642-108">Example 1: Enable tenant access</span></span>
```
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $ApimContext -Enabled $True
```

<span data-ttu-id="19642-109">這個命令會在指定的內容中啟用租使用者存取。</span><span class="sxs-lookup"><span data-stu-id="19642-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="19642-110">參數</span><span class="sxs-lookup"><span data-stu-id="19642-110">PARAMETERS</span></span>

### <span data-ttu-id="19642-111">-內容</span><span class="sxs-lookup"><span data-stu-id="19642-111">-Context</span></span>
<span data-ttu-id="19642-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="19642-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19642-113">-啟用</span><span class="sxs-lookup"><span data-stu-id="19642-113">-Enabled</span></span>
<span data-ttu-id="19642-114">指定此 Cmdlet 是否啟用或停用租使用者存取。</span><span class="sxs-lookup"><span data-stu-id="19642-114">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="19642-115">指定 $True 的值，以啟用或 $False 來停用。</span><span class="sxs-lookup"><span data-stu-id="19642-115">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19642-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19642-116">-PassThru</span></span>
<span data-ttu-id="19642-117">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的 **PsApiManagementAccessInformation** 。</span><span class="sxs-lookup"><span data-stu-id="19642-117">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="19642-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19642-118">-DefaultProfile</span></span>
<span data-ttu-id="19642-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="19642-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19642-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19642-120">CommonParameters</span></span>
<span data-ttu-id="19642-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="19642-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19642-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="19642-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19642-123">輸入</span><span class="sxs-lookup"><span data-stu-id="19642-123">INPUTS</span></span>

## <span data-ttu-id="19642-124">輸出</span><span class="sxs-lookup"><span data-stu-id="19642-124">OUTPUTS</span></span>

### <span data-ttu-id="19642-125">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="19642-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="19642-126">筆記</span><span class="sxs-lookup"><span data-stu-id="19642-126">NOTES</span></span>

## <span data-ttu-id="19642-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="19642-127">RELATED LINKS</span></span>

[<span data-ttu-id="19642-128">AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="19642-128">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


