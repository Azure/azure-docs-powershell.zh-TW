---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 1685b9607108fa0b7795fb0ed2c69eb94735fc5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908662"
---
# <span data-ttu-id="62b71-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="62b71-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="62b71-102">簡介</span><span class="sxs-lookup"><span data-stu-id="62b71-102">SYNOPSIS</span></span>
<span data-ttu-id="62b71-103">啟用或停用租使用者存取。</span><span class="sxs-lookup"><span data-stu-id="62b71-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="62b71-104">語法</span><span class="sxs-lookup"><span data-stu-id="62b71-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62b71-105">描述</span><span class="sxs-lookup"><span data-stu-id="62b71-105">DESCRIPTION</span></span>
<span data-ttu-id="62b71-106">**Set-AzApiManagementTenantAccess** Cmdlet 會啟用或停用租使用者存取。</span><span class="sxs-lookup"><span data-stu-id="62b71-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="62b71-107">例子</span><span class="sxs-lookup"><span data-stu-id="62b71-107">EXAMPLES</span></span>

### <span data-ttu-id="62b71-108">範例 1：啟用租使用者存取</span><span class="sxs-lookup"><span data-stu-id="62b71-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="62b71-109">此命令可在指定的內容中啟用租使用者存取。</span><span class="sxs-lookup"><span data-stu-id="62b71-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="62b71-110">參數</span><span class="sxs-lookup"><span data-stu-id="62b71-110">PARAMETERS</span></span>

### <span data-ttu-id="62b71-111">-內容</span><span class="sxs-lookup"><span data-stu-id="62b71-111">-Context</span></span>
<span data-ttu-id="62b71-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="62b71-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="62b71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b71-113">-DefaultProfile</span></span>
<span data-ttu-id="62b71-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="62b71-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62b71-115">-已啟用</span><span class="sxs-lookup"><span data-stu-id="62b71-115">-Enabled</span></span>
<span data-ttu-id="62b71-116">指定此 Cmdlet 是否啟用或停用租使用者存取。</span><span class="sxs-lookup"><span data-stu-id="62b71-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="62b71-117">指定要$True或$False的值。</span><span class="sxs-lookup"><span data-stu-id="62b71-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="62b71-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62b71-118">-PassThru</span></span>
<span data-ttu-id="62b71-119">表示此 Cmdlet 會傳回此 Cmdlet 修改的 **PsApiManagementAccesssInformation。**</span><span class="sxs-lookup"><span data-stu-id="62b71-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="62b71-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b71-120">CommonParameters</span></span>
<span data-ttu-id="62b71-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="62b71-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b71-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62b71-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b71-123">輸入</span><span class="sxs-lookup"><span data-stu-id="62b71-123">INPUTS</span></span>

### <span data-ttu-id="62b71-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="62b71-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="62b71-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="62b71-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="62b71-126">輸出</span><span class="sxs-lookup"><span data-stu-id="62b71-126">OUTPUTS</span></span>

### <span data-ttu-id="62b71-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="62b71-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="62b71-128">筆記</span><span class="sxs-lookup"><span data-stu-id="62b71-128">NOTES</span></span>

## <span data-ttu-id="62b71-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="62b71-129">RELATED LINKS</span></span>

[<span data-ttu-id="62b71-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="62b71-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


