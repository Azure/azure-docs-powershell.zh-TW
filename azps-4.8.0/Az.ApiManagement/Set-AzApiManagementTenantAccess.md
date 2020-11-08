---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 08bbb81998107a11a5996cb75a6fba8b760802db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128603"
---
# <span data-ttu-id="2adc0-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="2adc0-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="2adc0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2adc0-102">SYNOPSIS</span></span>
<span data-ttu-id="2adc0-103">啟用或停用租使用者存取。</span><span class="sxs-lookup"><span data-stu-id="2adc0-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="2adc0-104">句法</span><span class="sxs-lookup"><span data-stu-id="2adc0-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2adc0-105">說明</span><span class="sxs-lookup"><span data-stu-id="2adc0-105">DESCRIPTION</span></span>
<span data-ttu-id="2adc0-106">**AzApiManagementTenantAccess** Cmdlet 可啟用或停用租使用者存取。</span><span class="sxs-lookup"><span data-stu-id="2adc0-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="2adc0-107">示例</span><span class="sxs-lookup"><span data-stu-id="2adc0-107">EXAMPLES</span></span>

### <span data-ttu-id="2adc0-108">範例1：啟用租使用者存取</span><span class="sxs-lookup"><span data-stu-id="2adc0-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="2adc0-109">這個命令會在指定的內容中啟用租使用者存取。</span><span class="sxs-lookup"><span data-stu-id="2adc0-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="2adc0-110">參數</span><span class="sxs-lookup"><span data-stu-id="2adc0-110">PARAMETERS</span></span>

### <span data-ttu-id="2adc0-111">-內容</span><span class="sxs-lookup"><span data-stu-id="2adc0-111">-Context</span></span>
<span data-ttu-id="2adc0-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="2adc0-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2adc0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2adc0-113">-DefaultProfile</span></span>
<span data-ttu-id="2adc0-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2adc0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2adc0-115">-啟用</span><span class="sxs-lookup"><span data-stu-id="2adc0-115">-Enabled</span></span>
<span data-ttu-id="2adc0-116">指定此 Cmdlet 是否啟用或停用租使用者存取。</span><span class="sxs-lookup"><span data-stu-id="2adc0-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="2adc0-117">指定 $True 的值，以啟用或 $False 來停用。</span><span class="sxs-lookup"><span data-stu-id="2adc0-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="2adc0-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2adc0-118">-PassThru</span></span>
<span data-ttu-id="2adc0-119">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的 **PsApiManagementAccessInformation** 。</span><span class="sxs-lookup"><span data-stu-id="2adc0-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2adc0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2adc0-120">CommonParameters</span></span>
<span data-ttu-id="2adc0-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2adc0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2adc0-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2adc0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2adc0-123">輸入</span><span class="sxs-lookup"><span data-stu-id="2adc0-123">INPUTS</span></span>

### <span data-ttu-id="2adc0-124">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="2adc0-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2adc0-125">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="2adc0-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2adc0-126">輸出</span><span class="sxs-lookup"><span data-stu-id="2adc0-126">OUTPUTS</span></span>

### <span data-ttu-id="2adc0-127">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="2adc0-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="2adc0-128">筆記</span><span class="sxs-lookup"><span data-stu-id="2adc0-128">NOTES</span></span>

## <span data-ttu-id="2adc0-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="2adc0-129">RELATED LINKS</span></span>

[<span data-ttu-id="2adc0-130">AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="2adc0-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


